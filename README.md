# Missile-simulation
MATLAB/SIMULINK; surface to air missile; control law
  
## 导弹制导系统  
  导弹制导和控制系统是导弹的重要组成系统，是决定导弹最终精度和性能的关键系统。因此导弹的制导控制系统设计是目前导弹设计中的关键部分，本实验针对防空导弹打击高空目标，基于遥控制导中的三点法导引方式，设计导弹制导系统，在simulink平台上进行仿真验证，为今后深入研究导弹的制导和控制系统设计奠定理论基础。  
### 导弹制导系统的设计思路  
  导弹的制导系统通过测量目标的运动状态信息，控制导弹的飞行方向。因此对于制导系统来说其重点研究的是导弹的运动学关系，而不关心导弹的姿态变化和动力学关系。所以在进行导弹制导系统设计时通常将导弹作为一个质点研究，只考虑其在运动学中的速度、加速度和速度变化等因素。  
  由于制导系统设计决定了导弹在三维空间中的弹道，通过仿真可以确定导弹的脱靶量、机动能力和飞行轨迹等，因此对于制导系统的设计和仿真通常都是导弹制导控制系统设计的前一步骤。通过制导系统的设计达到了导弹设计的战术指标后，才考虑如何控制导弹使其实现制导系统所需要的过载。  
### 制导律的设计方法和步骤
  制导律的设计过程就是将导弹受到的力分解到纵向和侧向攻击平面内，分别在两个平面内设计制导律。通过在两个平面内的二维位置解算，最终可以构成在制导律控制下的导弹在三维空间中的运动轨迹。因此一般说来，三维空间的制导律步骤可以分为以下几步：  
①	分析导弹作战场景，选取合适的公共参考坐标系和两个攻击平面；  
②	分析导弹受到的力，将导弹的受力和速度矢量分解到两个攻击平面；  
③ 在攻击平面内，分析弹目相对运动关系，建立运动方程，设计攻击平面内的制导律；  
④ 在各自平面内按照运动方程搭建 Simulink 仿真框图；  
⑤ 合理设置仿真参数，进行数字仿真，注意观测仿真结果，检查模块中的错误；  
⑥ 输出各攻击平面内的仿真结果和关键数据，并将各自平面内的仿真结果按照空间关系合成到三维空间中，最终形成三维空间上的弹目飞行轨迹和实际过载；  
⑦	分析导弹飞行过程中的过载和脱靶量等指标，并对制导律进行评价。  

## 仿真模型  
  仿真框图分别由U2飞机目标仿真模块、SAM2导弹仿真模块、雷达制导站仿真模块以及存储显示与控制模块构成。  



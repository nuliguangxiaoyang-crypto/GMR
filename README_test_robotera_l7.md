## single amass motion file to robotera_l7 
python scripts/smplx_to_robot.py --smplx_file /home/era/rl/gmr_era/input_human_dataset/amass_smplx_G/ACCAD/Male2Walking_c3d/B10_-__Walk_turn_left_45_stageii.npz  --robot robotera_l7  --save_path output_humanoid_dataset/amass/robotera_l7/accd_B10_-__Walk_turn_left_45_stageii.pkl --rate_limit

## amass dataset to  robotera_l7
python scripts/smplx_to_robot_dataset.py   --src_folder /home/era/rl/gmr_era/input_human_dataset/amass_smplx_G/ACCAD/Male1Running_c3d   --tgt_folder /home/era/rl/GMR/output_humanoid_dataset/LALA   --robot robotera_l7


## lafan1 robotera_l7
python scripts/bvh_to_robot.py --bvh_file /home/era/rl/gmr_era/input_human_dataset/lafan1/dance1_subject1.bvh  --robot robotera_l7 --save_path output_humanoid_dataset/lafan1_dance1_subject1_robotera_l7.pkl --rate_limit



## gmr xsense robotera_l7
 python scripts/xsens_bvh_to_robot.py    --robot robotera_l7   --scale 0.01   --reset_to_zero   --bvh_format 3DSM   --bvh_file assets/xsens_bvh_test/251021_04_boxing_120Hz_cm_3DsMax.bvh   --save_path retargeting_data/robotera_l7/251021_04_boxing_120Hz_cm_3DsMax.pkl

## self xsense dataformat robotera_l7
 python scripts/xsens_bvh_to_robot.py     --bvh_file assets/xsense_bvh_v2_test/0311opensource-001.bvh   --robot robotera_l7    --save_path retargeting_data/robotera_l7/0311opensource-001.pkl  --reset_to_zero   --rate_limit   --scale 1.0

# Person Re-identification in Presence of Occlusion

This is the official code release for the paper titled: 
### Person Re-identification in Presence of Occlusion

Person Re-identification has been one of the crucial areas which received significant attention over the past few years. Automation of surveillance systems with high precision in monitoring under different scenarios is necessary.  Most of these systems fail in the presence of occlusion. Hence, we propose an approach that is robust and accurate even in the presence of occlusion. We first detect if a given frame is occluded initially. If there is occlusion, we employ ConvLSTM to reconstruct the occluded pixels for sequential data(video) to capture the spatio-temporal features from the previous frames, which results in improved reconstruction. For non-sequential data, we employ an Autoencoder. 
Finally, to fine-tune the reconstructed frames, we use a DC-GAN on top of both ConvLSTM & Autoencoder. This reconstruction strategy improved rank-1 reidentification accuracy on several publicly available datasets compared to other state-of-the-art techniques.

#### (a) Sequential Data(Videos): [Occlusion Detection ---> ConvLSTM + DC-GAN]

Sample ground-truth unoccluded sequential frames (first row), frames with synthetic occlusion (second row), reconstruction using **Conv-LSTM** (third row), and fine-tuning using **DC-GAN** (fourth row),<br>

<img src="Results/sequential_image_results.png" height="800"/>



#### (b) Non-Sequential Data(Images): [Occlusion Detection ---> Autoencoder + DC-GAN]

Sample ground-truth unoccluded non-sequential frames (first row), frames with synthetic occlusion (second row), reconstruction using **Autoencoder** (third row), and fine-tuning using **DC-GAN** (fourth row)

<img src="Results/non-sequential_results.png" height="800"/>

# Image-Steganography
<p>The project employs a novel approach to steganography by using a shuffled image as the carrier for the ciphertext. The ciphertext and shuffled image are combined to create a stego shuffled image. The stego image is then shuffled again to create a final shuffled image. The decryption process is simply the reverse of the encryption process, with the final shuffled image being deshuffled to extract the stego image. The stego image is then used to extract the ciphertext, which can be decrypted using the 3DES algorithm to retrieve the original message.</p>
<p>The use of the 3DES encryption algorithm ensures that the ciphertext is secure and cannot be easily deciphered by unauthorised parties. The image shuffler, on the other hand, ensures that the stego image is indistinguishable from the original image, making it difficult for anyone to detect the presence of hidden information.
Overall, this steganography project offers a robust and effective solution for secure communication and data storage, making it a valuable tool for anyone who values data privacy and security.</p>
<img width="769" alt="Process Flowchart" src="https://user-images.githubusercontent.com/24240285/231231273-3b835a5a-3aa5-4b4c-b7a5-e60918d40dac.png">
<h2>Architecture</h2>
<p>1. The plaintext message is first encrypted using the 3DES encryption algorithm. 3DES is a symmetric-key block cipher that encrypts data in blocks of 64 bits. The encryption key used in this project is a 192-bit key, which provides a high level of security.<br>
2. The image that is to be used for steganography is first shuffled using the image shuffling algorithm. This algorithm shuffles the pixels in the image in a random manner, which helps to hide the encrypted message more effectively.<br>
3. To embed the ciphertext into the shuffled image, the least significant bit (LSB) of each pixel is modified to represent a bit from the ciphertext.
This LSB modification ensures that the changes made to the image are imperceptible to the human eye.<br>
4. The shuffled image with the embedded ciphertext is now a stego shuffled image. This stego image is passed through the image shuffler again to further enhance the security of the hidden message. This step helps to prevent any attempts to extract the hidden message by reversing the image shuffling algorithm.<br>
5. The final step in the encryption process is to store the stego shuffled image, which now contains the encrypted message hidden within it. This image can be transmitted or stored like any other image, and the hidden message can be extracted only by someone who has the decryption key.<br>
6. The decryption process is the reverse of the encryption process. The stego shuffled image is first passed through the image shuffler to retrieve the original shuffled image.<br>
7. The LSB of each pixel in the retrieved shuffled image is then extracted to obtain the ciphertext. This ciphertext is decrypted using the 3DES decryption algorithm and the same key that was used for encryption.<br>
8. The decrypted message is now in plaintext form and can be read by the intended recipient.</p>
<h2> Steps to use</h2>
 You can directly start running the jupyter files with some minor changes to be done before that: <br>
1. Install pycryptodome library to your system or virtual environment for running the project by running the command <br>
<p align="center">pip3 install pycryptodome<br></p>
2. Also change the path for the cover image according to your system and also the path where the other images should be created in the further steps.<br>
3. The code will create new images at different steps as it proceeds and finally give a stego_image

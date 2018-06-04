---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WLAN_MAC_FRAME_STATISTICS structure


## -description


The <b>WLAN_MAC_FRAME_STATISTICS</b> structure contains information about sent and received MAC frames.


## -struct-fields




### -field ullTransmittedFrameCount

Contains the number of successfully transmitted MSDU/MMPDUs.


### -field ullReceivedFrameCount

Contains the number of successfully received MSDU/MMPDUs.


### -field ullWEPExcludedCount

Contains the number of frames discarded due to having a "Protected" status indicated in the frame control field.


### -field ullTKIPLocalMICFailures

Contains the number of MIC failures encountered while checking the integrity of packets received from the AP or peer station.


### -field ullTKIPReplays

Contains the number of TKIP replay errors detected.


### -field ullTKIPICVErrorCount

Contains the number of TKIP protected packets that the NIC failed to decrypt.


### -field ullCCMPReplays

Contains the number of received unicast fragments discarded by the replay mechanism.


### -field ullCCMPDecryptErrors

Contains the number of received fragments discarded by the CCMP decryption algorithm.


### -field ullWEPUndecryptableCount

Contains the number of WEP protected packets received for which a decryption key was not available on the NIC.


### -field ullWEPICVErrorCount

Contains the number of WEP protected packets the NIC failed to decrypt.


### -field ullDecryptSuccessCount

Contains the number of encrypted packets that the NIC has successfully decrypted.


### -field ullDecryptFailureCount

Contains the number of encrypted packets that the NIC has failed to decrypt.


## -see-also




<a href="https://msdn.microsoft.com/d66d89f1-bb12-4c2e-8c7a-a4eba008955d">WLAN_STATISTICS</a>
 

 


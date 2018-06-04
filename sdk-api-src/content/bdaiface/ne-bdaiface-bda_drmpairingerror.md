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

# BDA_DrmPairingError enumeration


## -description



Specifies the status of a DRM handshake between a tuner and the user's computer.




## -enum-fields




### -field BDA_DrmPairing_Succeeded

The handshake was successful.




### -field BDA_DrmPairing_HardwareFailure

A hardware failure occurred.


### -field BDA_DrmPairing_NeedRevocationData

The tuner could not obtain the certificate revocation list.




### -field BDA_DrmPairing_NeedIndiv

The tuner could not perform individualization.




### -field BDA_DrmPairing_Other

Network interface (SCTE 55-1).




### -field BDA_DrmPairing_DrmInitFailed

The handshake failed during the initialization step.


### -field BDA_DrmPairing_DrmNotPaired

The client has not requested a handshake or the handshake is still in progress.




### -field BDA_DrmPairing_DrmRePairSoon

The handshake was successful but will soon time out. The client should refresh the handshake soon.




### -field BDA_DrmPairing_Aborted


### -field BDA_DrmPairing_NeedSDKUpdate




## -see-also




<a href="https://msdn.microsoft.com/f6df89f3-6611-4aa3-ae74-babff88e23fa">BDA Reference</a>



<a href="https://msdn.microsoft.com/dff38609-9e90-491c-b8c4-33fd07471895">IBDA_DRM::GetDRMPairingStatus</a>
 

 


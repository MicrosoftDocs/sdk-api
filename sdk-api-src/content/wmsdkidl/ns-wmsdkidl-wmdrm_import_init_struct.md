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

# WMDRM_IMPORT_INIT_STRUCT structure


## -description



The <b>WMDRM_IMPORT_INIT_STRUCT</b> structure holds the encrypted session key and content key used in importing protected content.




## -struct-fields




### -field dwVersion

Version.


### -field cbEncryptedSessionKeyMessage

Size of the encrypted session key message in bytes.


### -field pbEncryptedSessionKeyMessage

Address of a buffer containing the encrypted session key message. This message is contained in a field of a <a href="https://msdn.microsoft.com/2dd1e8ec-a25f-4ced-8f1b-286534c66ebf">WMDRM_IMPORT_SESSION_KEY</a> structure. The message and its associated key data are both encrypted with the Windows Media DRM machine public key.


### -field cbEncryptedKeyMessage

Size of the encrypted key message in bytes.


### -field pbEncryptedKeyMessage

Address of a buffer containing the encrypted key message. This message is contained in a field of a <a href="https://msdn.microsoft.com/29a0f98d-96a3-46b2-a67c-dbb23449e927">WMDRM_IMPORT_CONTENT_KEY</a> structure. The message and its associated key data are both encrypted with the Windows Media DRM machine public key.


## -remarks



This structure is used to initialize protected stream sample writing in a call to the <a href="https://msdn.microsoft.com/42208d02-8384-494d-b7ae-53072b795723">IWMDRMWriter3::SetProtectStreamSamples</a> method.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 


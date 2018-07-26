---
UID: NF:xapo.IXAPO.GetRegistrationProperties
title: IXAPO::GetRegistrationProperties
author: windows-sdk-content
description: Returns the registration properties of an XAPO.
old-location: xaudio2\ixapo_interface_getregistrationproperties.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.GetRegistrationProperties(XAPO_REGISTRATION_PROPERTIES)
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetRegistrationProperties, GetRegistrationProperties method [XAudio2 Audio Mixing APIs], GetRegistrationProperties method [XAudio2 Audio Mixing APIs],IXAPO interface, IXAPO interface [XAudio2 Audio Mixing APIs],GetRegistrationProperties method, IXAPO.GetRegistrationProperties, IXAPO::GetRegistrationProperties, xapo/IXAPO::GetRegistrationProperties, xaudio2.ixapo_interface_getregistrationproperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xapo.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: XAPO_BUFFER_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPO.h
api_name:
 - IXAPO.GetRegistrationProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAPO::GetRegistrationProperties


## -description


Returns the registration properties of an XAPO. 


## -parameters




### -param ppRegistrationProperties

Receives a pointer to a <a href="https://msdn.microsoft.com/library/Ee419210(v=VS.85).aspx">XAPO_REGISTRATION_PROPERTIES</a> structure containing the registration properties the XAPO was created with; use <a href="https://msdn.microsoft.com/library/Ee419206(v=VS.85).aspx">XAPOFree</a> to free the structure. 


## -returns



Returns S_OK if successful; returns an error code otherwise.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/library/Ee415893(v=VS.85).aspx">IXAPO</a>
 

 


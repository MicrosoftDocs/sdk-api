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

# WofGetDriverVersion function


## -description


Used to query the version of the driver used to support a particular provider.


## -parameters




### -param FileOrVolumeHandle [in]

A handle to a file or volume opened with <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> or a similar API.


### -param Provider [in]

Indicates which provider the version query is intended for. Multiple versions of Wof may exist on the same volume at the same time for different providers. 



### -param WofVersion [out]

Pointer to a ULONG which will contain the version upon successful completion of this function. 


## -returns



This function returns an HRESULT indicating success or the reason for failure. If no driver is attached on the specified volume for the specified provider, the function will fail with HRESULT_FROM_WIN32(ERROR_INVALID_FUNCTION). 






## -remarks



On successful completion, the WofVersion value is updated to reflect the version of the WOF driver. This value includes the major and minor version numbers of the operating system in the high-order word, and the build number of the operating system in the low-order word. The major version can be extracted with HIBYTE(HIWORD(WofVersion)); the minor version can be extracted with LOBYTE(HIWORD(WofVersion)); the build number can be extracted with LOWORD(WofVersion). 

QuickInfo





## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt426734">FSCTL_GET_WOF_VERSION</a>
 

 


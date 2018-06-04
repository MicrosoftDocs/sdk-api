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

# ITpmVirtualSmartCardManager::DestroyVirtualSmartCard


## -description


Destroys the TPM virtual smart card that has the given instance ID.


## -parameters




### -param pszInstanceId




### -param pStatusCallback [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/6CB62E42-16FD-453F-9566-B4DFCDAC7368">ITpmVirtualSmartCardManagerStatusCallback</a> interface. The TPM virtual smart card manager uses this callback interface to communicate the progress and errors during creation of the virtual smart card. If the <i>pStatusCallback</i> parameter is <b>NULL</b>, no progress is reported to the client before the operation completes.


### -param pfNeedReboot [out]

Pointer to a Boolean value to receive whether the requested operation needs to reboot the client computer.


#### - pszInstanceID [in]

Instance identifier of the TPM virtual smart card that is returned from a successful <a href="https://msdn.microsoft.com/C80C4DE2-0C43-40A5-81E6-7036A0B8DEB7">CreateVirtualSmartCard</a> method call. 


## -returns



If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns a Win32 error code. 




## -see-also




<a href="https://msdn.microsoft.com/46CC703B-14A2-4588-BA13-837C76B70F07">ITpmVirtualSmartCardManager</a>
 

 


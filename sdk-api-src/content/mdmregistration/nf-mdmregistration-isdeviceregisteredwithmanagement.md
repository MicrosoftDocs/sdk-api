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

# IsDeviceRegisteredWithManagement function


## -description


Checks whether the device is registered with an MDM service. If the device is registered, 
    it also returns the user principal name (UPN) of the registered user.


## -parameters




### -param pfIsDeviceRegisteredWithManagement [out]

Address of a <b>BOOL</b> indicates whether the device is registered.


### -param cchUPN [in, optional]

Contains the maximum length that can be returned through the <i>pszUPN</i> 
      parameter.


### -param pszUPN [out, optional]

Optional address of a buffer that receives the  <b>NULL</b>-terminated Unicode string 
      containing the UPN of the user registered with the management service. If <i>pszUPN</i> is 
      <b>NULL</b> then the <b>BOOL</b> pointed to by the 
      <i>pfIsDeviceRegisteredWithManagement</i> parameter is updated to indicate whether the device 
      is registered and the function returns <b>ERROR_SUCCESS</b>.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and the 
       <b>BOOL</b> pointed to by the 
       <i>pfIsDeviceRegisteredWithManagement</i> parameter contains <b>TRUE</b> 
       or <b>FALSE</b>. If <b>TRUE</b>, the Unicode string pointed to by the 
       <i>pszUPN</i> parameter contains the UPN of the registered user. If the function fails, the 
       returned value describes the error. Possible values include those listed at 
       <a href="https://msdn.microsoft.com/1f42ed5e-e221-47ec-a019-ed06c05d55d0">MDM Registration Error Values</a>.

If the buffer size indicated by the <i>cchUPN</i> parameter is too small then the call will fail with 
       <b>STRSAFE_E_INSUFFICIENT_BUFFER</b> but the <b>BOOL</b> pointed to by 
       the <i>pfIsDeviceRegisteredWithManagement</i> parameter will be updated to indicate whether 
       the device is registered.




## -see-also




<a href="https://msdn.microsoft.com/1f42ed5e-e221-47ec-a019-ed06c05d55d0">MDM Registration Error Values</a>



<a href="https://msdn.microsoft.com/1b063a56-f59f-4b02-949f-c8b6bbf45a13">MDM Registration Functions</a>
 

 


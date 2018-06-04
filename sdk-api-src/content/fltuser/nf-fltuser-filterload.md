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

# FilterLoad function


## -description


The <b>FilterLoad</b> function dynamically loads a minifilter driver into the system. 


## -parameters




### -param lpFilterName [in]

Pointer to a null-terminated wide-character string that specifies the service name of the minifilter driver. This parameter is required and cannot be <b>NULL</b> or an empty string. 


## -returns



<b>FilterLoad</b> returns S_OK if successful. Otherwise, it returns one of the following error values: 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32 (ERROR_ALREADY_EXISTS)</b></b></dt>
</dl>
</td>
<td width="60%">
The minifilter driver is already running. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32 (ERROR_FILE_NOT_FOUND)</b></b></dt>
</dl>
</td>
<td width="60%">
No matching minifilter driver was found. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>
        HRESULT_FROM_WIN32 (ERROR_SERVICE_ALREADY_RUNNING)</b></b></dt>
</dl>
</td>
<td width="60%">
The minifilter driver is already running. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>
        HRESULT_FROM_WIN32 (ERROR_BAD_EXE_FORMAT)</b></b></dt>
</dl>
</td>
<td width="60%">
The load image for the minifilter driver specified by <i>lpFilterName</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>
        HRESULT_FROM_WIN32 (ERROR_BAD_DRIVER)</b></b></dt>
</dl>
</td>
<td width="60%">
The load image for the minifilter driver specified by <i>lpFilterName</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>
        HRESULT_FROM_WIN32 (ERROR_INVALID_IMAGE_HASH)</b></b></dt>
</dl>
</td>
<td width="60%">
The minifilter driver has an invalid digital signature.

</td>
</tr>
</table>
 




## -remarks



<b>FilterLoad</b> is the Win32 equivalent of <a href="https://msdn.microsoft.com/library/windows/hardware/ff543366">FltLoadFilter</a>. 

A user-mode application that has a dependency on a kernel-mode minifilter driver can load the minifilter driver by calling <b>FilterLoad</b>. 

Callers of <b>FilterLoad</b> must have <b>SeLoadDriverPrivilege</b> (the LUID of SE_LOAD_DRIVER_PRIVILEGE) to load or unload a minifilter driver. This privilege is named by the SE_LOAD_DRIVER_NAME name constant. (Privileges are described in the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0 documentation.) 

To unload the minifilter driver, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff541516">FilterUnload</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541516">FilterUnload</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543366">FltLoadFilter</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=139085">HRESULT_FROM_WIN32</a>
 

 


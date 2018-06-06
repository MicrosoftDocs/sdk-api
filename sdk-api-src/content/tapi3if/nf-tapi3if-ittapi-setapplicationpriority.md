---
UID: NF:tapi3if.ITTAPI.SetApplicationPriority
title: ITTAPI::SetApplicationPriority
author: windows-sdk-content
description: The SetApplicationPriority method allows an application to set its priority in the handoff priority list for a particular media type or Assisted Telephony request mode, or to remove itself from the priority list.
old-location: tapi3\ittapi_setapplicationpriority.htm
old-project: Tapi
ms.assetid: ca049695-02d0-4b30-ad1f-60cdbf0a4dbd
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITTAPI interface [TAPI 2.2],SetApplicationPriority method, ITTAPI.SetApplicationPriority, ITTAPI::SetApplicationPriority, SetApplicationPriority, SetApplicationPriority method [TAPI 2.2], SetApplicationPriority method [TAPI 2.2],ITTAPI interface, _tapi3_ittapi_setapplicationpriority, tapi3.ittapi_setapplicationpriority, tapi3if/ITTAPI::SetApplicationPriority
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITTAPI.SetApplicationPriority
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTAPI::SetApplicationPriority


## -description


The 
<b>SetApplicationPriority</b> method allows an application to set its priority in the handoff priority list for a particular media type or Assisted Telephony request mode, or to remove itself from the priority list.


## -parameters




### -param pAppFilename [in]

Pointer to <b>BSTR</b> containing name of application.


### -param lMediaType [in]

Media associated with application.


### -param fPriority [in]

The new priority for the application. If the value VARIANT_FALSE is passed, the application is removed from the priority list for the specified media or request mode (if it was already not present, no error is generated). If the value VARIANT_TRUE is passed, the application is inserted as the highest-priority application for the media or request mode (and removed from a lower-priority position, if it was already in the list).


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



The application must use 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for the <i>pAppFilename</i> parameter and use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variable is no longer needed.

The Priorities that are set with <b>SetApplicationPriority</b> will persist across reboots of the system or restarts of tapisrv. The <a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a> function opens the line with no specified call priorities. By default, the highest priority application will be the one that first called <b>ITTAPI::RegisterCallNotifications</b>.




## -see-also




<a href="https://msdn.microsoft.com/02579638-fafd-4c4a-91a3-460d7ebf6917">ITBasicCallControl::HandoffIndirect</a>



<a href="https://msdn.microsoft.com/75d641c7-dbf8-4ae2-b16b-2757e890d32b">ITTAPI</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>
 

 


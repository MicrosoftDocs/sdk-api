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

# MsiNotifySidChangeW function


## -description


The <b>MsiNotifySidChange</b> function notifies and updates the Windows Installer internal information  with changes to  user SIDs.


## -parameters




### -param pOldSid

TBD


### -param pNewSid

TBD




#### - szNewSid [in]

Null-terminated string that specifies the string value of the new security identifier(SID).


#### - szOldSid [in]

Null-terminated string that specifies the string value of the previous security identifier(SID).


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter is passed to the function. This error returned if any of the parameters is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory was available.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Internal failure during execution.


</td>
</tr>
</table>
 




## -remarks



<b>Windows Installer 2.0 and Windows Installer 3.0:  </b>Not supported. This function is available beginning with Windows Installer 3.1.




## -see-also




<a href="https://msdn.microsoft.com/35be6da4-2a20-4a7a-9f6e-0420cd5a227e">Not Supported in Windows Installer 3.0 and earlier</a>
 

 


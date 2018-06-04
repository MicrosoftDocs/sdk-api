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

# SCardAudit function


## -description


The <b>SCardAudit</b> function writes event messages to the Windows application log Microsoft-Windows-SmartCard-Audit/Authentication.


## -parameters




### -param hContext [in]

Handle that identifies the resource manager context. The resource manager context can be set by a previous call to the <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a> function. This parameter cannot be <b>NULL</b>. 


### -param dwEvent [in]

The event to log.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_AUDIT_CHV_FAILURE"></a><a id="scard_audit_chv_failure"></a><dl>
<dt><b>SCARD_AUDIT_CHV_FAILURE</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
A smart card holder verification (CHV) attempt failed.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_AUDIT_CHV_SUCCESS"></a><a id="scard_audit_chv_success"></a><dl>
<dt><b>SCARD_AUDIT_CHV_SUCCESS</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
A smart card holder verification (CHV) attempt succeeded.

</td>
</tr>
</table>
 


## -returns



This function returns different values depending on whether it succeeds or fails.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Success</b></dt>
</dl>
</td>
<td width="60%">
SCARD_S_SUCCESS.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Failure</b></dt>
</dl>
</td>
<td width="60%">
An error code. For more information, see 
<a href="authentication_return_values.htm">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



This function is not redirected. An application calling the <b>SCardAudit</b> function from within a Remote Desktop session will log the event on the remote system.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// hContext was set by a previous call to SCardEstablishContext.
lReturn = SCardAudit (hContext,
                      SCARD_AUDIT_CHV_SUCCESS);

if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardAudit - %x\n", lReturn);
    // Take appropriate action
}
</pre>
</td>
</tr>
</table></span></div>



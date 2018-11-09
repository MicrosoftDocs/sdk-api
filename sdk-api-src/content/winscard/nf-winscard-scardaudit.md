---
UID: NF:winscard.SCardAudit
title: SCardAudit function
author: windows-sdk-content
description: Writes event messages to the Windows application log Microsoft-Windows-SmartCard-Audit/Authentication.
old-location: security\scardaudit.htm
tech.root: secauthn
ms.assetid: 5D30DC71-C69A-403B-8658-99C80C268E90
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: SCARD_AUDIT_CHV_FAILURE, SCARD_AUDIT_CHV_SUCCESS, SCardAudit, SCardAudit function [Security], security.scardaudit, winscard/SCardAudit
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
api_name:
 - SCardAudit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/Aa374738(v=VS.85).aspx">Smart Card Return Values</a>.

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



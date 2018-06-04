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

# IESLicenseRenewalResultEvent::GetRenewalResultCode


## -description


Gets a constant from a Protected Broadcast Driver Architecture (PBDA) <b>LicenseRenewalResult</b> event that indicates which step in the renewal process caused the renewal to succeed or fail. A client can call the <a href="https://msdn.microsoft.com/0c57e4e4-ee93-4e86-b1f8-eed5dd5aa931">IsRenewalSuccessful</a> method to determine if the renewal was successful, and then call this method to get information about the reason for any failure.


## -parameters




### -param pdwRenewalResultCode [out, retval]

Receives the result code. The result code indicates the license renewal step that failed and can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>LBE_RenewalStage_Invalid</dt>
</dl>
</td>
<td width="60%">
Received license was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>LRE_RenewalStage_RenewalFailed</dt>
</dl>
</td>
<td width="60%">
Renewal attempt failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>LRE_RenewalStage_CheckForRenewableLicense</dt>
</dl>
</td>
<td width="60%">
Renewal attempt failed during the check for a renewable license.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>LRE_RenewalStage_RenewLicenseAtTuner</dt>
</dl>
</td>
<td width="60%">
Renewal attempt failed at the tuner.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>LRE_RenewalStage_StoreLicenseInDRM</dt>
</dl>
</td>
<td width="60%">
Renewal attempt failed during license storage.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>LRE_RenewalStage_RenewalSuccessful</dt>
</dl>
</td>
<td width="60%">
License renewal was successful.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6f9cbec4-7934-41fc-b387-3f45aa273a72">IESLicenseRenewalResultEvent</a>
 

 


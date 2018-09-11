---
UID: NF:adhoc.IDot11AdHocSecuritySettings.GetDot11AuthAlgorithm
title: IDot11AdHocSecuritySettings::GetDot11AuthAlgorithm
author: windows-sdk-content
description: Gets the authentication algorithm associated with the security settings.
old-location: nwifi\idot11adhocsecuritysettings_getdot11authalgorithm.htm
tech.root: nativewifi
ms.assetid: 87ba445a-1ad7-49da-aa61-ed72d118e517
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDot11AuthAlgorithm, GetDot11AuthAlgorithm method [NativeWIFI], GetDot11AuthAlgorithm method [NativeWIFI],IDot11AdHocSecuritySettings interface, IDot11AdHocSecuritySettings interface [NativeWIFI],GetDot11AuthAlgorithm method, IDot11AdHocSecuritySettings.GetDot11AuthAlgorithm, IDot11AdHocSecuritySettings::GetDot11AuthAlgorithm, adhoc/IDot11AdHocSecuritySettings::GetDot11AuthAlgorithm, nwifi.idot11adhocsecuritysettings_getdot11authalgorithm
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocSecuritySettings.GetDot11AuthAlgorithm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDot11AdHocSecuritySettings::GetDot11AuthAlgorithm


## -description


Gets the authentication algorithm associated with the security settings. The authentication algorithm is used to authenticate machines and users connecting to the ad hoc network associated with an interface. 


## -parameters




### -param pAuth [in, out]

A pointer to a <a href="https://msdn.microsoft.com/6e28fb8f-a429-4b6c-a057-737bbadb0a95">DOT11_ADHOC_AUTH_ALGORITHM</a> value that specifies the authentication algorithm.


## -returns



Possible return values include, but are not limited to, the following.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value pointed to by <i>pAuth</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The pointer <i>pAuth</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/55b78a98-ad25-4646-b325-73d770d602b3">IDot11AdHocSecuritySettings</a>



<a href="https://msdn.microsoft.com/46bf39e3-351f-41c2-8f68-886fce8a83bd">IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm</a>
 

 


---
UID: NF:adhoc.IDot11AdHocSecuritySettings.GetDot11CipherAlgorithm
title: IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm
author: windows-sdk-content
description: Gets the cipher algorithm associated with the security settings.
old-location: nwifi\idot11adhocsecuritysettings_getdot11cipheralgorithm.htm
old-project: nativewifi
ms.assetid: 46bf39e3-351f-41c2-8f68-886fce8a83bd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDot11CipherAlgorithm, GetDot11CipherAlgorithm method [NativeWIFI], GetDot11CipherAlgorithm method [NativeWIFI],IDot11AdHocSecuritySettings interface, IDot11AdHocSecuritySettings interface [NativeWIFI],GetDot11CipherAlgorithm method, IDot11AdHocSecuritySettings.GetDot11CipherAlgorithm, IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm, adhoc/IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm, nwifi.idot11adhocsecuritysettings_getdot11cipheralgorithm
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: adhoc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocSecuritySettings.GetDot11CipherAlgorithm
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm


## -description


Gets the cipher algorithm associated with the security settings. The cipher algorithm is used to encrypt and decrypt information sent on the ad hoc network associated with an interface.


## -parameters




### -param pCipher [in, out]

A pointer to a <a href="https://msdn.microsoft.com/2ea8173d-f528-4065-90ce-71a455a6b35f">DOT11_ADHOC_CIPHER_ALGORITHM</a> value that specifies the cipher algorithm.


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
The value pointed to by <i>pCipher</i> is invalid.

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
The pointer <i>pCipher</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/55b78a98-ad25-4646-b325-73d770d602b3">IDot11AdHocSecuritySettings</a>



<a href="https://msdn.microsoft.com/87ba445a-1ad7-49da-aa61-ed72d118e517">IDot11AdHocSecuritySettings::GetDot11AuthAlgorithm</a>
 

 


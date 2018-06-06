---
UID: NF:mfidl.IMFNetCredentialCache.GetCredential
title: IMFNetCredentialCache::GetCredential
author: windows-sdk-content
description: Retrieves the credential object for the specified URL.
old-location: mf\imfnetcredentialcache_getcredential.htm
old-project: medfound
ms.assetid: 7e095445-354a-4fbb-b354-bf87eb77552f
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 7e095445-354a-4fbb-b354-bf87eb77552f, GetCredential, GetCredential method [Media Foundation], GetCredential method [Media Foundation],IMFNetCredentialCache interface, IMFNetCredentialCache interface [Media Foundation],GetCredential method, IMFNetCredentialCache.GetCredential, IMFNetCredentialCache::GetCredential, mf.imfnetcredentialcache_getcredential, mfidl/IMFNetCredentialCache::GetCredential
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetCredentialCache.GetCredential
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFNetCredentialCache::GetCredential


## -description



Retrieves the credential object for the specified URL.




## -parameters




### -param pszUrl [in]

A null-terminated wide-character string containing the URL for which the credential is needed.


### -param pszRealm [in]

A null-terminated wide-character string containing the realm for the authentication.


### -param dwAuthenticationFlags [in]

Bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/4a2f5537-b78c-49a6-9b66-d3ca34c3fc67">MFNetAuthenticationFlags</a> enumeration.


### -param ppCred [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/d202e7bc-9ce0-4861-8552-5a4d599b1661">IMFNetCredential</a> interface. The caller must release the interface.


### -param pdwRequirementsFlags






#### - pdwFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/9257d1d7-7ccb-4172-82f0-3694ebb9d487">MFNetCredentialRequirements</a> enumeration.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d02e26e7-e99c-4be7-8495-830eff2f1554">IMFNetCredentialCache</a>
 

 


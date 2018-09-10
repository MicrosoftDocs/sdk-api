---
UID: NF:certenroll.IX509PrivateKey.Delete
title: IX509PrivateKey::Delete
author: windows-sdk-content
description: Releases the handle of the cryptographic service provider (CSP) or the handle of the Cryptography API:\_Next Generation (CNG) key storage provider (KSP) and deletes the key from disk or smart card.
old-location: security\ix509privatekey_delete_method.htm
tech.root: SecCertEnroll
ms.assetid: 0f319e20-d993-480e-846d-0912bb854415
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Delete, Delete method [Security], Delete method [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],Delete method, IX509PrivateKey.Delete, IX509PrivateKey::Delete, certenroll/IX509PrivateKey::Delete, security.ix509privatekey_delete_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509PrivateKey.Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509PrivateKey::Delete


## -description


The <b>Delete</b> method releases the handle of the cryptographic service provider (CSP) or the handle of the Cryptography API: Next Generation (CNG) key storage provider (KSP) and deletes the key from disk or smart card.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>CERTSRV_E_PROPERTY_EMPTY</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The CSP could not be found.

</td>
</tr>
</table>
 




## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa378935(v=VS.85).aspx">Close</a> method if you only want to close the provider handles. The <b>Delete</b> method does not delete the <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> instance.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a>
 

 


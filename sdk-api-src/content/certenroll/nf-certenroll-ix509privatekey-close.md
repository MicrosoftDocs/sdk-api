---
UID: NF:certenroll.IX509PrivateKey.Close
title: IX509PrivateKey::Close
author: windows-sdk-content
description: Releases the handle of the cryptographic service provider (CSP) or the handle of the Cryptography API:\_Next Generation (CNG) key storage provider (KSP).
old-location: security\ix509privatekey_close_method.htm
old-project: seccertenroll
ms.assetid: c4ed2375-0d50-4cb5-b0c4-c80962e22c9c
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: Close, Close method [Security], Close method [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],Close method, IX509PrivateKey.Close, IX509PrivateKey::Close, certenroll/IX509PrivateKey::Close, security.ix509privatekey_close_method
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509PrivateKey.Close
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509PrivateKey::Close


## -description


The <b>Close</b> method releases the handle of the cryptographic service provider (CSP) or the handle of the Cryptography API: Next Generation (CNG) key storage provider (KSP).


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This method does not delete the key from storage or the <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> instance. For more information, see the <a href="https://msdn.microsoft.com/0f319e20-d993-480e-846d-0912bb854415">Delete</a> method.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 


---
UID: NF:certenroll.IX509PrivateKey.ExportPublicKey
title: IX509PrivateKey::ExportPublicKey
author: windows-sdk-content
description: Exports the public key portion of the asymmetric key pair.
old-location: security\ix509privatekey_exportpublickey_method.htm
tech.root: seccertenroll
ms.assetid: 4ebcba09-1fea-4d21-8315-3570eaf6d42d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ExportPublicKey, ExportPublicKey method [Security], ExportPublicKey method [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],ExportPublicKey method, IX509PrivateKey.ExportPublicKey, IX509PrivateKey::ExportPublicKey, certenroll/IX509PrivateKey::ExportPublicKey, security.ix509privatekey_exportpublickey_method
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
 - IX509PrivateKey.ExportPublicKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509PrivateKey::ExportPublicKey


## -description


The <b>ExportPublicKey</b> method exports the public key portion of the asymmetric key pair.


## -parameters




### -param ppPublicKey [out]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a> interface that represents the key.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



You must call <a href="https://msdn.microsoft.com/965e3bf8-22b9-4015-8fb2-102c5f7b1cb5">Open</a> or <a href="https://msdn.microsoft.com/e8c6564a-6009-437e-9b83-3711e43a7374">Create</a> to open the private key before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 


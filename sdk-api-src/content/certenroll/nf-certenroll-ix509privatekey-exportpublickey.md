---
UID: NF:certenroll.IX509PrivateKey.ExportPublicKey
title: IX509PrivateKey::ExportPublicKey (certenroll.h)
author: windows-sdk-content
description: Exports the public key portion of the asymmetric key pair.
old-location: security\ix509privatekey_exportpublickey_method.htm
tech.root: seccertenroll
ms.assetid: 4ebcba09-1fea-4d21-8315-3570eaf6d42d
ms.author: windowssdkdev
ms.date: 12/05/2018
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
ms.custom: 19H1
---

# IX509PrivateKey::ExportPublicKey


## -description


The <b>ExportPublicKey</b> method exports the public key portion of the asymmetric key pair.


## -parameters




### -param ppPublicKey [out]

Address of a variable that receives a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a> interface that represents the key.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



You must call <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-open">Open</a> or <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-create">Create</a> to open the private key before calling this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
 

 


---
UID: NF:casetup.ICertSrvSetup.CAImportPFX
title: ICertSrvSetup::CAImportPFX (casetup.h)
description: Imports a certification authority (CA) certificate and its associated private key into the local computer store.
helpviewer_keywords: ["CAImportPFX","CAImportPFX method [Security]","CAImportPFX method [Security]","ICertSrvSetup interface","ICertSrvSetup interface [Security]","CAImportPFX method","ICertSrvSetup.CAImportPFX","ICertSrvSetup::CAImportPFX","casetup/ICertSrvSetup::CAImportPFX","security.icertsrvsetup_caimportpfx"]
old-location: security\icertsrvsetup_caimportpfx.htm
tech.root: security
ms.assetid: a661b74b-04ba-49b9-bde2-3e368ae6228e
ms.date: 12/05/2018
ms.keywords: CAImportPFX, CAImportPFX method [Security], CAImportPFX method [Security],ICertSrvSetup interface, ICertSrvSetup interface [Security],CAImportPFX method, ICertSrvSetup.CAImportPFX, ICertSrvSetup::CAImportPFX, casetup/ICertSrvSetup::CAImportPFX, security.icertsrvsetup_caimportpfx
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertSrvSetup::CAImportPFX
 - casetup/ICertSrvSetup::CAImportPFX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetup.CAImportPFX
---

# ICertSrvSetup::CAImportPFX


## -description

The <b>CAImportPFX</b> method imports a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) certificate and its associated <a href="/windows/desktop/SecGloss/p-gly">private key</a> into the local computer store. This method does not change the state of the <b>CCertSrvSetup</b> object.

## -parameters

### -param bstrFileName [in]

A string that contains the name of a PFX file used to import a <a href="/windows/desktop/SecGloss/p-gly">private key</a>.

### -param bstrPasswd [in]

A string that contains a password for the PFX file.

### -param bOverwriteExistingKey [in]

A value that indicates whether to overwrite an existing key of the same name.

### -param ppVal [out]

The address of a pointer to an <a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetupkeyinformation">ICertSrvSetupKeyInformation</a> interface that can be used to set properties of the imported private key.

## -remarks

The <b>CAImportPFX</b> method uses the input parameters to decrypt and decode a PFX file and then installs the key and <a href="/windows/desktop/SecGloss/c-gly">certificate</a> in the local computer store. If the certificate satisfies the following criteria and after installation of the key, the method returns an <a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetupkeyinformation">ICertSrvSetupKeyInformation</a> object to the caller.

<ul>
<li>Contains an AT_SIGNATURE key that matches the key in the private key container.
</li>
<li>Is self-signed or has basic constraints for a CA.</li>
<li>Passes chain validation but might have an offline revocation error.
</li>
</ul>
If the PFX file contains multiple certificates and keys, <b>CAImportPFX</b> installs all of the certificates and keys; however, the returned <a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetupkeyinformation">ICertSrvSetupKeyInformation</a> object only contains properties of the last CA certificate in the file. When the caller finishes using the <b>ICertSrvSetupKeyInformation</b> object, the caller must release it by using the <a href="/windows/win32/api/unknwn/nf-unknwn-iunknown-release">Release</a> method.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>
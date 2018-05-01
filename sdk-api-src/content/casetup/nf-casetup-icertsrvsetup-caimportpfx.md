---
UID: NF:casetup.ICertSrvSetup.CAImportPFX
title: ICertSrvSetup::CAImportPFX method
author: windows-driver-content
description: Imports a certification authority (CA) certificate and its associated private key into the local computer store.
old-location: security\icertsrvsetup_caimportpfx.htm
old-project: SecCrypto
ms.assetid: a661b74b-04ba-49b9-bde2-3e368ae6228e
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: CAImportPFX method [Security], CAImportPFX method [Security], ICertSrvSetup interface, CAImportPFX,ICertSrvSetup.CAImportPFX, ICertSrvSetup, ICertSrvSetup interface [Security], CAImportPFX method, ICertSrvSetup::CAImportPFX, casetup/ICertSrvSetup::CAImportPFX, security.icertsrvsetup_caimportpfx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: CEPSetupProperty
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certocm.dll
api_name:
-	ICertSrvSetup.CAImportPFX
product: Windows
targetos: Windows
req.lib: 
req.dll: Certocm.dll
req.irql: 
---

# ICertSrvSetup::CAImportPFX method


## -description


The <b>CAImportPFX</b> method imports a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) certificate and its associated <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> into the local computer store. This method does not change the state of the <b>CCertSrvSetup</b> object.


## -parameters




### -param bstrFileName [in]

A string that contains the name of a PFX file used to import a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>.


### -param bstrPasswd [in]

A string that contains a password for the PFX file.


### -param bOverwriteExistingKey [in]

A value that indicates whether to overwrite an existing key of the same name.


### -param ppVal [out]

The address of a pointer to an <a href="https://msdn.microsoft.com/d27c9ba5-ddee-4c9c-b812-e61b974b515a">ICertSrvSetupKeyInformation</a> interface that can be used to set properties of the imported private key.


## -remarks



The <b>CAImportPFX</b> method uses the input parameters to decrypt and decode a PFX file and then installs the key and <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a> in the local computer store. If the certificate satisfies the following criteria and after installation of the key, the method returns an <a href="https://msdn.microsoft.com/d27c9ba5-ddee-4c9c-b812-e61b974b515a">ICertSrvSetupKeyInformation</a> object to the caller.

<ul>
<li>Contains an AT_SIGNATURE key that matches the key in the private key container.
</li>
<li>Is self-signed or has basic constraints for a CA.</li>
<li>Passes chain validation but might have an offline revocation error.
</li>
</ul>
If the PFX file contains multiple certificates and keys, <b>CAImportPFX</b> installs all of the certificates and keys; however, the returned <a href="https://msdn.microsoft.com/d27c9ba5-ddee-4c9c-b812-e61b974b515a">ICertSrvSetupKeyInformation</a> object only contains properties of the last CA certificate in the file. When the caller finishes using the <b>ICertSrvSetupKeyInformation</b> object, the caller must release it by using the <a href="http://go.microsoft.com/fwlink/p/?linkid=96732">Release</a> method.




## -see-also




<a href="https://msdn.microsoft.com/6792a0d6-d304-481d-a97b-5fb7033c7eae">ICertSrvSetup</a>
 

 


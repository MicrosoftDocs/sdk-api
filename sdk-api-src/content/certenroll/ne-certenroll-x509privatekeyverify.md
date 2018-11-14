---
UID: NE:certenroll.X509PrivateKeyVerify
title: X509PrivateKeyVerify
author: windows-sdk-content
description: Specifies whether a user interface is displayed during private key verification and whether verification can proceed if the cryptographic provider is a smart card provider.
old-location: security\x509privatekeyverify.htm
tech.root: SecCertEnroll
ms.assetid: 23466035-6554-490f-ad46-e97ba5a5d996
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: VerifyAllowUI, VerifyNone, VerifySilent, VerifySmartCardNone, VerifySmartCardSilent, X509PrivateKeyVerify, X509PrivateKeyVerify enumeration [Security], certenroll/VerifyAllowUI, certenroll/VerifyNone, certenroll/VerifySilent, certenroll/VerifySmartCardNone, certenroll/VerifySmartCardSilent, certenroll/X509PrivateKeyVerify, security.x509privatekeyverify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - X509PrivateKeyVerify
product: Windows
targetos: Windows
req.typenames: X509PrivateKeyVerify
req.redist: 
---

# X509PrivateKeyVerify enumeration


## -description


The <b>X509PrivateKeyVerify</b> enumeration specifies whether a user interface is displayed during <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> verification and whether verification can proceed if the cryptographic provider is a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> provider. This enumeration is used by the <a href="https://msdn.microsoft.com/4a792c39-71a7-4289-854d-98e6f749a526">Verify</a> method on the <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> interface.


## -enum-fields




### -field VerifyNone

No option is identified.


### -field VerifySilent

The method does not display a user interface.


### -field VerifySmartCardNone

No verification occurs if the key is stored on a smart card (the CSP or KSP is a smart card provider).


### -field VerifySmartCardSilent

The method does not display a user interface if the key is stored on a smart card (the CSP or KSP is a smart card provider).


### -field VerifyAllowUI

The method displays a user interface.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 


---
UID: NE:certenroll.X509PrivateKeyVerify
title: X509PrivateKeyVerify
author: windows-sdk-content
description: Specifies whether a user interface is displayed during private key verification and whether verification can proceed if the cryptographic provider is a smart card provider.
old-location: security\x509privatekeyverify.htm
old-project: seccertenroll
ms.assetid: 23466035-6554-490f-ad46-e97ba5a5d996
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: VerifyAllowUI, VerifyNone, VerifySilent, VerifySmartCardNone, VerifySmartCardSilent, X509PrivateKeyVerify, X509PrivateKeyVerify enumeration [Security], certenroll/VerifyAllowUI, certenroll/VerifyNone, certenroll/VerifySilent, certenroll/VerifySmartCardNone, certenroll/VerifySmartCardSilent, certenroll/X509PrivateKeyVerify, security.x509privatekeyverify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: certenroll.h
req.include-header: 
req.redist: 
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
req.typenames: X509PrivateKeyVerify
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
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# X509PrivateKeyVerify enumeration


## -description


The <b>X509PrivateKeyVerify</b> enumeration specifies whether a user interface is displayed during <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a> verification and whether verification can proceed if the cryptographic provider is a <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">smart card</a> provider. This enumeration is used by the <a href="https://msdn.microsoft.com/en-us/library/Aa379038(v=VS.85).aspx">Verify</a> method on the <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> interface.


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




<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a>
 

 


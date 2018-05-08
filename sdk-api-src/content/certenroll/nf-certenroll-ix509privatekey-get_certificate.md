---
UID: NF:certenroll.IX509PrivateKey.get_Certificate
title: IX509PrivateKey::get_Certificate
author: windows-driver-content
description: Specifies or retrieves a byte array that contains the certificate associated with the private key.
old-location: security\ix509privatekey_certificate_property.htm
old-project: SecCertEnroll
ms.assetid: 035615f1-2dc7-47d7-98e4-7b5b0924030f
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: Certificate property [Security], Certificate property [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],Certificate property, IX509PrivateKey.Certificate, IX509PrivateKey.get_Certificate, IX509PrivateKey::Certificate, IX509PrivateKey::get_Certificate, IX509PrivateKey::put_Certificate, certenroll/IX509PrivateKey::Certificate, certenroll/IX509PrivateKey::get_Certificate, certenroll/IX509PrivateKey::put_Certificate, get_Certificate, security.ix509privatekey_certificate_property
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509PrivateKey.Certificate
-	IX509PrivateKey.get_Certificate
-	IX509PrivateKey.put_Certificate
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509PrivateKey::get_Certificate


## -description


The <b>Certificate</b> property specifies or retrieves a byte array that contains the certificate associated with the private key.  The byte array is represented by a Unicode-encoded string.

This property is read/write.


## -parameters


## -remarks



If the key is not open when you specify a  certificate, the certificate will be set when the key is opened. For more information, see the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> method.

The <b>Certificate</b> property compares the public key associated with the <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object to the public key included in the certificate. The two keys must match.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 


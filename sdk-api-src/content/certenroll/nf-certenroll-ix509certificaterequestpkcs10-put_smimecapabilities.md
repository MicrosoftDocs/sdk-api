---
UID: NF:certenroll.IX509CertificateRequestPkcs10.put_SmimeCapabilities
title: IX509CertificateRequestPkcs10::put_SmimeCapabilities
author: windows-sdk-content
description: Specifies or retrieves a Boolean value that tells the Encode method whether to create an IX509ExtensionSmimeCapabilities collection that identifies the encryption capabilities supported by the computer.
old-location: security\ix509certificaterequestpkcs10_smimecapabilities_property.htm
old-project: seccertenroll
ms.assetid: 5aa027d7-3c31-4b70-92a5-d15d2c410366
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],SmimeCapabilities property, IX509CertificateRequestPkcs10.SmimeCapabilities, IX509CertificateRequestPkcs10.put_SmimeCapabilities, IX509CertificateRequestPkcs10::SmimeCapabilities, IX509CertificateRequestPkcs10::get_SmimeCapabilities, IX509CertificateRequestPkcs10::put_SmimeCapabilities, SmimeCapabilities property [Security], SmimeCapabilities property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::SmimeCapabilities, certenroll/IX509CertificateRequestPkcs10::get_SmimeCapabilities, certenroll/IX509CertificateRequestPkcs10::put_SmimeCapabilities, put_SmimeCapabilities, security.ix509certificaterequestpkcs10_smimecapabilities_property
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
 - IX509CertificateRequestPkcs10.SmimeCapabilities
 - IX509CertificateRequestPkcs10.get_SmimeCapabilities
 - IX509CertificateRequestPkcs10.put_SmimeCapabilities
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs10::put_SmimeCapabilities


## -description


The <b>SmimeCapabilities</b> property specifies or retrieves a Boolean value that tells the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method whether to create an <a href="https://msdn.microsoft.com/06dca62d-282b-4bdd-bc8d-4d2e6eb226b5">IX509ExtensionSmimeCapabilities</a> collection that  identifies the encryption capabilities supported by the computer. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



Multipurpose Internet Mail Extensions (MIME) is a specification for formatting binary data into text so that it can be sent in email. Secure/Multipurpose Internet Mail Extensions (S/MIME) is a standard for encrypting and signing a MIME message.

The  <b>SmimeCapabilities</b> extension, represented by an <a href="https://msdn.microsoft.com/06dca62d-282b-4bdd-bc8d-4d2e6eb226b5">IX509ExtensionSmimeCapabilities</a> object, is used when sending and receiving encrypted email messages to report the recipient's decryption capabilities to the sender. This enables the sender to choose the most secure algorithm supported by both the sender and recipient.

If you did not set the <a href="https://msdn.microsoft.com/3a7847b6-52b4-4058-8113-cbc3b9101a5b">SuppressDefaults</a> property before calling the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method, the <b>SmimeCapabilities</b> extension is added by default and the available symmetric algorithm OIDs are enumerated and added to the extension value. Set the <b>SmimeCapabilities</b> property before calling <b>Encode</b>.




## -see-also




<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
 

 


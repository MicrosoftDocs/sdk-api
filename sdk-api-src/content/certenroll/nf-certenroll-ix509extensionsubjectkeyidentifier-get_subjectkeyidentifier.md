---
UID: NF:certenroll.IX509ExtensionSubjectKeyIdentifier.get_SubjectKeyIdentifier
title: IX509ExtensionSubjectKeyIdentifier::get_SubjectKeyIdentifier
author: windows-driver-content
description: Retrieves a byte array that contains the key identifier.
old-location: security\ix509extensionsubjectkeyidentifier_subjectkeyidentifier_property.htm
old-project: SecCertEnroll
ms.assetid: b055197c-d659-4b92-92b2-b7955beac08a
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IX509ExtensionSubjectKeyIdentifier interface [Security],SubjectKeyIdentifier property, IX509ExtensionSubjectKeyIdentifier.SubjectKeyIdentifier, IX509ExtensionSubjectKeyIdentifier.get_SubjectKeyIdentifier, IX509ExtensionSubjectKeyIdentifier::SubjectKeyIdentifier, IX509ExtensionSubjectKeyIdentifier::get_SubjectKeyIdentifier, SubjectKeyIdentifier property [Security], SubjectKeyIdentifier property [Security],IX509ExtensionSubjectKeyIdentifier interface, certenroll/IX509ExtensionSubjectKeyIdentifier::SubjectKeyIdentifier, certenroll/IX509ExtensionSubjectKeyIdentifier::get_SubjectKeyIdentifier, get_SubjectKeyIdentifier, security.ix509extensionsubjectkeyidentifier_subjectkeyidentifier_property
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
-	IX509ExtensionSubjectKeyIdentifier.SubjectKeyIdentifier
-	IX509ExtensionSubjectKeyIdentifier.get_SubjectKeyIdentifier
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionSubjectKeyIdentifier::get_SubjectKeyIdentifier


## -description


The <b>SubjectKeyIdentifier</b> property retrieves a byte array that contains the key identifier. The byte array is represented by a Unicode-encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/5886187d-33b1-4151-a01f-de263c41c27b">InitializeDecode</a> method or the <a href="https://msdn.microsoft.com/0faf3567-3908-473e-9f5c-392991ea668c">InitializeEncode</a> method to initialize the <a href="https://msdn.microsoft.com/dcf28967-65e0-4669-b1b1-b3d42f1b3d6b">IX509ExtensionSubjectKeyIdentifier</a> object. You can also call the <a href="https://msdn.microsoft.com/library/windows/hardware/mt158256">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property to retrieve the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/dcf28967-65e0-4669-b1b1-b3d42f1b3d6b">IX509ExtensionSubjectKeyIdentifier</a>
 

 


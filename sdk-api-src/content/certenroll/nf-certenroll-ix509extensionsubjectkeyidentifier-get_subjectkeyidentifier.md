---
UID: NF:certenroll.IX509ExtensionSubjectKeyIdentifier.get_SubjectKeyIdentifier
title: IX509ExtensionSubjectKeyIdentifier::get_SubjectKeyIdentifier
author: windows-sdk-content
description: Retrieves a byte array that contains the key identifier.
old-location: security\ix509extensionsubjectkeyidentifier_subjectkeyidentifier_property.htm
tech.root: seccertenroll
ms.assetid: b055197c-d659-4b92-92b2-b7955beac08a
ms.author: windowssdkdev
ms.date: 12/5/2018
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
 - IX509ExtensionSubjectKeyIdentifier.SubjectKeyIdentifier
 - IX509ExtensionSubjectKeyIdentifier.get_SubjectKeyIdentifier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionSubjectKeyIdentifier::get_SubjectKeyIdentifier


## -description


The <b>SubjectKeyIdentifier</b> property retrieves a byte array that contains the key identifier. The byte array is represented by a Unicode-encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa378217(v=VS.85).aspx">InitializeDecode</a> method or the <a href="https://msdn.microsoft.com/en-us/library/Aa378220(v=VS.85).aspx">InitializeEncode</a> method to initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa378215(v=VS.85).aspx">IX509ExtensionSubjectKeyIdentifier</a> object. You can also call the <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property to retrieve the <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378215(v=VS.85).aspx">IX509ExtensionSubjectKeyIdentifier</a>
 

 


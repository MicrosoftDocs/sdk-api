---
UID: NF:certenroll.IX509ExtensionBasicConstraints.get_IsCA
title: IX509ExtensionBasicConstraints::get_IsCA
author: windows-sdk-content
description: Retrieves a Boolean value that identifies whether the subject of the certificate is a certification authority (CA).
old-location: security\ix509extensionbasicconstraints_isca_property.htm
tech.root: SecCertEnroll
ms.assetid: 1547d015-b497-4f91-acc2-4cbb2a69709f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IX509ExtensionBasicConstraints interface [Security],IsCA property, IX509ExtensionBasicConstraints.IsCA, IX509ExtensionBasicConstraints.get_IsCA, IX509ExtensionBasicConstraints::IsCA, IX509ExtensionBasicConstraints::get_IsCA, IsCA property [Security], IsCA property [Security],IX509ExtensionBasicConstraints interface, certenroll/IX509ExtensionBasicConstraints::IsCA, certenroll/IX509ExtensionBasicConstraints::get_IsCA, get_IsCA, security.ix509extensionbasicconstraints_isca_property
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
 - IX509ExtensionBasicConstraints.IsCA
 - IX509ExtensionBasicConstraints.get_IsCA
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509ExtensionBasicConstraints.get_IsCA
: 
---

# IX509ExtensionBasicConstraints::get_IsCA


## -description


The <b>IsCA</b> property retrieves a Boolean value that identifies whether the subject of the certificate is a certification authority (CA).

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa378112(v=VS.85).aspx">InitializeEncode</a> method or the <a href="https://msdn.microsoft.com/en-us/library/Aa378109(v=VS.85).aspx">InitializeDecode</a> method to initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa378108(v=VS.85).aspx">IX509ExtensionBasicConstraints</a> object and specify the <b>IsCA</b> property. You can also call the <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property to retrieve the <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378108(v=VS.85).aspx">IX509ExtensionBasicConstraints</a>
 

 


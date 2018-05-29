---
UID: NF:certenroll.IX509ExtensionAlternativeNames.get_AlternativeNames
title: IX509ExtensionAlternativeNames::get_AlternativeNames
author: windows-sdk-content
description: Retrieves a collection of subject alternative names.
old-location: security\ix509extensionalternativenames_alternativenames_property.htm
old-project: SecCertEnroll
ms.assetid: 816afa9d-2283-4e17-ad12-ee53e5353d83
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: AlternativeNames property [Security], AlternativeNames property [Security],IX509ExtensionAlternativeNames interface, IX509ExtensionAlternativeNames interface [Security],AlternativeNames property, IX509ExtensionAlternativeNames.AlternativeNames, IX509ExtensionAlternativeNames.get_AlternativeNames, IX509ExtensionAlternativeNames::AlternativeNames, IX509ExtensionAlternativeNames::get_AlternativeNames, certenroll/IX509ExtensionAlternativeNames::AlternativeNames, certenroll/IX509ExtensionAlternativeNames::get_AlternativeNames, get_AlternativeNames, security.ix509extensionalternativenames_alternativenames_property
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509ExtensionAlternativeNames.AlternativeNames
-	IX509ExtensionAlternativeNames.get_AlternativeNames
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionAlternativeNames::get_AlternativeNames


## -description


The <b>AlternativeNames</b> property retrieves a collection of subject alternative names.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/e520b2b4-c181-4fb1-98e8-f159bd0d31b4">InitializeEncode</a> method or the <a href="https://msdn.microsoft.com/a314dfac-fe17-4e33-b528-491a2622e80c">InitializeDecode</a> method to initialize the collection. You can also call the <a href="https://msdn.microsoft.com/library/windows/hardware/mt158256">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property to retrieve the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/facfcc85-c1ca-47a1-90a6-10522b15cc65">IX509ExtensionAlternativeNames</a>
 

 


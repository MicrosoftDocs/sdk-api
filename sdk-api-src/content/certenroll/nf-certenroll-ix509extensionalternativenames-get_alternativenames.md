---
UID: NF:certenroll.IX509ExtensionAlternativeNames.get_AlternativeNames
title: IX509ExtensionAlternativeNames::get_AlternativeNames
author: windows-sdk-content
description: Retrieves a collection of subject alternative names.
old-location: security\ix509extensionalternativenames_alternativenames_property.htm
tech.root: SecCertEnroll
ms.assetid: 816afa9d-2283-4e17-ad12-ee53e5353d83
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AlternativeNames property [Security], AlternativeNames property [Security],IX509ExtensionAlternativeNames interface, IX509ExtensionAlternativeNames interface [Security],AlternativeNames property, IX509ExtensionAlternativeNames.AlternativeNames, IX509ExtensionAlternativeNames.get_AlternativeNames, IX509ExtensionAlternativeNames::AlternativeNames, IX509ExtensionAlternativeNames::get_AlternativeNames, certenroll/IX509ExtensionAlternativeNames::AlternativeNames, certenroll/IX509ExtensionAlternativeNames::get_AlternativeNames, get_AlternativeNames, security.ix509extensionalternativenames_alternativenames_property
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
 - IX509ExtensionAlternativeNames.AlternativeNames
 - IX509ExtensionAlternativeNames.get_AlternativeNames
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionAlternativeNames::get_AlternativeNames


## -description


The <b>AlternativeNames</b> property retrieves a collection of subject alternative names.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa378090(v=VS.85).aspx">InitializeEncode</a> method or the <a href="https://msdn.microsoft.com/en-us/library/Aa378087(v=VS.85).aspx">InitializeDecode</a> method to initialize the collection. You can also call the <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property to retrieve the <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378081(v=VS.85).aspx">IX509ExtensionAlternativeNames</a>
 

 


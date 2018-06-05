---
UID: NF:certenroll.IX509ExtensionSmimeCapabilities.get_SmimeCapabilities
title: IX509ExtensionSmimeCapabilities::get_SmimeCapabilities
author: windows-sdk-content
description: Retrieves a collection of ISmimeCapability objects.
old-location: security\ix509extensionsmimecapabilities_smimecapabilities.htm
old-project: SecCertEnroll
ms.assetid: 6e3ce718-16f9-47df-aff9-38e922fe505c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509ExtensionSmimeCapabilities interface [Security],SmimeCapabilities property, IX509ExtensionSmimeCapabilities.SmimeCapabilities, IX509ExtensionSmimeCapabilities.get_SmimeCapabilities, IX509ExtensionSmimeCapabilities::SmimeCapabilities, IX509ExtensionSmimeCapabilities::get_SmimeCapabilities, SmimeCapabilities property [Security], SmimeCapabilities property [Security],IX509ExtensionSmimeCapabilities interface, certenroll/IX509ExtensionSmimeCapabilities::SmimeCapabilities, certenroll/IX509ExtensionSmimeCapabilities::get_SmimeCapabilities, get_SmimeCapabilities, security.ix509extensionsmimecapabilities_smimecapabilities
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509ExtensionSmimeCapabilities.SmimeCapabilities
-	IX509ExtensionSmimeCapabilities.get_SmimeCapabilities
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionSmimeCapabilities::get_SmimeCapabilities


## -description


The <b>SmimeCapabilities</b> property retrieves a collection of <a href="https://msdn.microsoft.com/3cfbb16f-88fa-41f1-b719-cd5e8ad636cc">ISmimeCapability</a> objects.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/731e3c93-699b-4a99-8520-294f3134aa66">InitializeEncode</a> method or the <a href="https://msdn.microsoft.com/9b89b9aa-3e71-4511-8e5a-1fe2165fa672">InitializeDecode</a> method to initialize the <b>SMIMECapabilities</b> extension.  You can also call the <a href="https://msdn.microsoft.com/library/windows/hardware/mt158256">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property to retrieve the OID associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/06dca62d-282b-4bdd-bc8d-4d2e6eb226b5">IX509ExtensionSmimeCapabilities</a>
 

 


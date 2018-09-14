---
UID: NF:certenroll.IX509ExtensionSmimeCapabilities.get_SmimeCapabilities
title: IX509ExtensionSmimeCapabilities::get_SmimeCapabilities
author: windows-sdk-content
description: Retrieves a collection of ISmimeCapability objects.
old-location: security\ix509extensionsmimecapabilities_smimecapabilities.htm
tech.root: seccertenroll
ms.assetid: 6e3ce718-16f9-47df-aff9-38e922fe505c
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509ExtensionSmimeCapabilities interface [Security],SmimeCapabilities property, IX509ExtensionSmimeCapabilities.SmimeCapabilities, IX509ExtensionSmimeCapabilities.get_SmimeCapabilities, IX509ExtensionSmimeCapabilities::SmimeCapabilities, IX509ExtensionSmimeCapabilities::get_SmimeCapabilities, SmimeCapabilities property [Security], SmimeCapabilities property [Security],IX509ExtensionSmimeCapabilities interface, certenroll/IX509ExtensionSmimeCapabilities::SmimeCapabilities, certenroll/IX509ExtensionSmimeCapabilities::get_SmimeCapabilities, get_SmimeCapabilities, security.ix509extensionsmimecapabilities_smimecapabilities
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
 - IX509ExtensionSmimeCapabilities.SmimeCapabilities
 - IX509ExtensionSmimeCapabilities.get_SmimeCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionSmimeCapabilities::get_SmimeCapabilities


## -description


The <b>SmimeCapabilities</b> property retrieves a collection of <a href="https://msdn.microsoft.com/en-us/library/Aa377045(v=VS.85).aspx">ISmimeCapability</a> objects.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa378185(v=VS.85).aspx">InitializeEncode</a> method or the <a href="https://msdn.microsoft.com/en-us/library/Aa378181(v=VS.85).aspx">InitializeDecode</a> method to initialize the <b>SMIMECapabilities</b> extension.  You can also call the <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property to retrieve the OID associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378177(v=VS.85).aspx">IX509ExtensionSmimeCapabilities</a>
 

 


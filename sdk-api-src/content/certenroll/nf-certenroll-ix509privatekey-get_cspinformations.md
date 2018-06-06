---
UID: NF:certenroll.IX509PrivateKey.get_CspInformations
title: IX509PrivateKey::get_CspInformations
author: windows-sdk-content
description: Specifies or retrieves a collection of ICspInformation objects that contain information about the available cryptographic providers that support the public key algorithm associated with the private key.
old-location: security\ix509privatekey_cspinformations.htm
old-project: SecCertEnroll
ms.assetid: 81cf4689-0cd6-4185-9242-ef26de9161a1
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: CspInformations property [Security], CspInformations property [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],CspInformations property, IX509PrivateKey.CspInformations, IX509PrivateKey.get_CspInformations, IX509PrivateKey::CspInformations, IX509PrivateKey::get_CspInformations, IX509PrivateKey::put_CspInformations, certenroll/IX509PrivateKey::CspInformations, certenroll/IX509PrivateKey::get_CspInformations, certenroll/IX509PrivateKey::put_CspInformations, get_CspInformations, security.ix509privatekey_cspinformations
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
 - IX509PrivateKey.CspInformations
 - IX509PrivateKey.get_CspInformations
 - IX509PrivateKey.put_CspInformations
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509PrivateKey::get_CspInformations


## -description


The <b>CspInformations</b> property specifies or retrieves a collection of <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> objects that contain information about the available cryptographic providers  that support the public key algorithm associated with the private key. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



The enrollment process expects the <a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a> collection to include all providers installed on the client computer. You should therefore not attempt to set this property to a subset of the installed providers. We recommend that you create  an empty  collection and call <a href="https://msdn.microsoft.com/f44af323-41fb-46d6-88ed-15d465fc8815">AddAvailableCsps</a> to  populate it. Build this collection once and set it on all top level request objects (or the private key if you are using the <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object directly) to avoid the cost of creating multiple collections. An <b>ICspInformations</b> collection is large.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 


---
UID: NF:certenroll.IX509PrivateKey.get_CspInformations
title: IX509PrivateKey::get_CspInformations
author: windows-sdk-content
description: Specifies or retrieves a collection of ICspInformation objects that contain information about the available cryptographic providers that support the public key algorithm associated with the private key.
old-location: security\ix509privatekey_cspinformations.htm
tech.root: SecCertEnroll
ms.assetid: 81cf4689-0cd6-4185-9242-ef26de9161a1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CspInformations property [Security], CspInformations property [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],CspInformations property, IX509PrivateKey.CspInformations, IX509PrivateKey.get_CspInformations, IX509PrivateKey::CspInformations, IX509PrivateKey::get_CspInformations, IX509PrivateKey::put_CspInformations, certenroll/IX509PrivateKey::CspInformations, certenroll/IX509PrivateKey::get_CspInformations, certenroll/IX509PrivateKey::put_CspInformations, get_CspInformations, security.ix509privatekey_cspinformations
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
 - IX509PrivateKey.CspInformations
 - IX509PrivateKey.get_CspInformations
 - IX509PrivateKey.put_CspInformations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509PrivateKey::get_CspInformations


## -description


The <b>CspInformations</b> property specifies or retrieves a collection of <a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a> objects that contain information about the available cryptographic providers  that support the public key algorithm associated with the private key. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



The enrollment process expects the <a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a> collection to include all providers installed on the client computer. You should therefore not attempt to set this property to a subset of the installed providers. We recommend that you create  an empty  collection and call <a href="https://msdn.microsoft.com/en-us/library/Aa375969(v=VS.85).aspx">AddAvailableCsps</a> to  populate it. Build this collection once and set it on all top level request objects (or the private key if you are using the <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> object directly) to avoid the cost of creating multiple collections. An <b>ICspInformations</b> collection is large.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a>
 

 


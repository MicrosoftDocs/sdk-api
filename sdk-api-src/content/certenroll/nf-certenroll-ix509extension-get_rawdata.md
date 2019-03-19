---
UID: NF:certenroll.IX509Extension.get_RawData
title: IX509Extension::get_RawData (certenroll.h)
author: windows-sdk-content
description: Retrieves a byte array that contains the extension value.
old-location: security\ix509extension_rawdata_property.htm
tech.root: seccertenroll
ms.assetid: 779ad765-e767-4594-afdb-49fe79a8e64b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509Extension interface [Security],RawData property, IX509Extension.RawData, IX509Extension.get_RawData, IX509Extension::RawData, IX509Extension::get_RawData, RawData property [Security], RawData property [Security],IX509Extension interface, certenroll/IX509Extension::RawData, certenroll/IX509Extension::get_RawData, get_RawData, security.ix509extension_rawdata_property
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
 - IX509Extension.RawData
 - IX509Extension.get_RawData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509Extension::get_RawData


## -description


The <b>RawData</b> property retrieves a byte array that contains the extension value. The byte array is represented by a Unicode-encoded string.

This property is read-only.


## -parameters


## -remarks



A certificate extension is defined by an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) structure, and the extension is encoded into a byte array by using DER. The byte array is returned in a string to simplify use in languages other than C++. You can use the <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration to specify the type of Unicode encoding to apply to the string. You can call the <a href="https://msdn.microsoft.com/a01a371b-7dc2-4204-8029-269ac4a9c0d5">Initialize</a> method to specify the extension.




## -see-also




<a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>
 

 


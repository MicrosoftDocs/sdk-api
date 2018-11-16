---
UID: NF:cryptxml.CryptXmlGetReference
title: CryptXmlGetReference function
author: windows-sdk-content
description: Returns the Reference element specified by the supplied handle.
old-location: security\cryptxmlgetreference.htm
tech.root: SecCrypto
ms.assetid: aa482331-872d-4b51-a975-62d832a369fc
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CryptXmlGetReference, CryptXmlGetReference function [Security], cryptxml/CryptXmlGetReference, security.cryptxmlgetreference
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: cryptxml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cryptxml.lib
req.dll: Cryptxml.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptxml.dll
api_name:
 - CryptXmlGetReference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CryptXmlGetReference
: 
---

# CryptXmlGetReference function


## -description


The <b>CryptXmlGetReference</b> function returns the   <b>Reference</b> element specified by the supplied handle.


## -parameters




### -param hCryptXml [in]

The handle of the <b>Reference</b> element to retrieve.


### -param ppStruct [out]

A pointer to a pointer to a <a href="https://msdn.microsoft.com/af16af5a-b1e5-4250-bdb1-f3fceb1830b9">CRYPT_XML_REFERENCE</a> structure that contains the returned <b>Reference</b> element.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.




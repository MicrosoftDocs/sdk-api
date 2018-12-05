---
UID: NF:cryptxml.CryptXmlGetSignature
title: CryptXmlGetSignature function
author: windows-sdk-content
description: Returns an XML Signature element.
old-location: security\cryptxmlgetsignature.htm
tech.root: seccrypto
ms.assetid: ef6748eb-1d3b-43e0-9525-2b588c2ae13f
ms.author: windowssdkdev
ms.date: 12/04/2018
ms.keywords: CryptXmlGetSignature, CryptXmlGetSignature function [Security], cryptxml/CryptXmlGetSignature, security.cryptxmlgetsignature
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
 - CryptXmlGetSignature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptXmlGetSignature function


## -description


The <b>CryptXmlGetSignature</b> function returns an XML <b>Signature</b> element. 


## -parameters




### -param hCryptXml [in]

The handle of the <b>Signature</b> element. 


### -param ppStruct [out]

A pointer to a  pointer to a <a href="https://msdn.microsoft.com/d9930946-aec0-42a4-949f-af8b2e9c6e6c">CRYPT_XML_SIGNATURE</a> structure to receive the signature.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.




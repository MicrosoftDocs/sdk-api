---
UID: NF:cryptxml.CryptXmlGetDocContext
title: CryptXmlGetDocContext function
author: windows-sdk-content
description: Returns the document context specified by the supplied handle.
old-location: security\cryptxmlgetdoccontext.htm
tech.root: SecCrypto
ms.assetid: 0532c790-381c-4a91-8211-725b0fa73830
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CryptXmlGetDocContext, CryptXmlGetDocContext function [Security], cryptxml/CryptXmlGetDocContext, security.cryptxmlgetdoccontext
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
 - CryptXmlGetDocContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptXmlGetDocContext function


## -description


The <b>CryptXmlGetDocContext</b> function returns the  document context specified by the supplied handle.


## -parameters




### -param hCryptXml [in]

The handle of the document context to retrieve. 


### -param ppStruct [out]

A pointer to a pointer to a  <a href="https://msdn.microsoft.com/b57cccb1-b26f-4710-b888-f864cc9ae3be">CRYPT_XML_DOC_CTXT</a> structure that contains the returned document context.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.




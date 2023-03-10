---
UID: NF:cryptxml.CryptXmlGetDocContext
title: CryptXmlGetDocContext function (cryptxml.h)
description: Returns the document context specified by the supplied handle.
helpviewer_keywords: ["CryptXmlGetDocContext","CryptXmlGetDocContext function [Security]","cryptxml/CryptXmlGetDocContext","security.cryptxmlgetdoccontext"]
old-location: security\cryptxmlgetdoccontext.htm
tech.root: security
ms.assetid: 0532c790-381c-4a91-8211-725b0fa73830
ms.date: 12/05/2018
ms.keywords: CryptXmlGetDocContext, CryptXmlGetDocContext function [Security], cryptxml/CryptXmlGetDocContext, security.cryptxmlgetdoccontext
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptXmlGetDocContext
 - cryptxml/CryptXmlGetDocContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptxml.dll
api_name:
 - CryptXmlGetDocContext
---

# CryptXmlGetDocContext function


## -description

The <b>CryptXmlGetDocContext</b> function returns the  document context specified by the supplied handle.

## -parameters

### -param hCryptXml [in]

The handle of the document context to retrieve.

### -param ppStruct [out]

A pointer to a pointer to a  <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_doc_ctxt">CRYPT_XML_DOC_CTXT</a> structure that contains the returned document context.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.
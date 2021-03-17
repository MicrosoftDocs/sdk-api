---
UID: NF:cryptxml.CryptXmlGetStatus
title: CryptXmlGetStatus function (cryptxml.h)
description: Returns a CRYPT_XML_STATUS structure that contains status information about the object specified by the supplied handle.
helpviewer_keywords: ["CryptXmlGetStatus","CryptXmlGetStatus function [Security]","cryptxml/CryptXmlGetStatus","security.cryptxmlgetstatus"]
old-location: security\cryptxmlgetstatus.htm
tech.root: security
ms.assetid: 685a87dc-36e9-464a-988e-de907d2dae41
ms.date: 12/05/2018
ms.keywords: CryptXmlGetStatus, CryptXmlGetStatus function [Security], cryptxml/CryptXmlGetStatus, security.cryptxmlgetstatus
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
 - CryptXmlGetStatus
 - cryptxml/CryptXmlGetStatus
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
 - CryptXmlGetStatus
---

# CryptXmlGetStatus function


## -description

The <b>CryptXmlGetStatus</b> function returns a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_status">CRYPT_XML_STATUS</a> structure that contains status information about the object specified by the supplied handle.

## -parameters

### -param hCryptXml

A handle to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_signature">CRYPT_XML_SIGNATURE</a> structure, an array 
of <b>CRYPT_XML_SIGNATURE</b> structures , a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_reference">CRYPT_XML_REFERENCE</a> structure, or a  Manifest object about which to get status information.

### -param pStatus

A pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_status">CRYPT_XML_STATUS</a> structure to receive the returned status information.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.
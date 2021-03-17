---
UID: NC:cryptxml.PFN_CRYPT_XML_DATA_PROVIDER_CLOSE
title: PFN_CRYPT_XML_DATA_PROVIDER_CLOSE (cryptxml.h)
description: Releases the data provider.
helpviewer_keywords: ["PFN_CRYPT_XML_DATA_PROVIDER_CLOSE","PFN_CRYPT_XML_DATA_PROVIDER_CLOSE callback","PFN_CRYPT_XML_DATA_PROVIDER_CLOSE callback function [Security]","cryptxml/PFN_CRYPT_XML_DATA_PROVIDER_CLOSE","security.pfn_crypt_xml_data_provider_close"]
old-location: security\pfn_crypt_xml_data_provider_close.htm
tech.root: security
ms.assetid: 886fbe92-f9ab-49d4-968a-afeadbf2f030
ms.date: 12/05/2018
ms.keywords: PFN_CRYPT_XML_DATA_PROVIDER_CLOSE, PFN_CRYPT_XML_DATA_PROVIDER_CLOSE callback, PFN_CRYPT_XML_DATA_PROVIDER_CLOSE callback function [Security], cryptxml/PFN_CRYPT_XML_DATA_PROVIDER_CLOSE, security.pfn_crypt_xml_data_provider_close
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_CRYPT_XML_DATA_PROVIDER_CLOSE
 - cryptxml/PFN_CRYPT_XML_DATA_PROVIDER_CLOSE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Cryptxml.h
api_name:
 - PFN_CRYPT_XML_DATA_PROVIDER_CLOSE
---

# PFN_CRYPT_XML_DATA_PROVIDER_CLOSE callback function


## -description

The <i>PFN_CRYPT_XML_DATA_PROVIDER_CLOSE</i> callback function releases the data provider.

## -parameters

### -param pvCallbackState [in, out]

An application defined argument for the callback function.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.


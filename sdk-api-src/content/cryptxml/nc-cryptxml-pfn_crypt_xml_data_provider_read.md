---
UID: NC:cryptxml.PFN_CRYPT_XML_DATA_PROVIDER_READ
title: PFN_CRYPT_XML_DATA_PROVIDER_READ (cryptxml.h)
description: Reads XML data.
helpviewer_keywords: ["PFN_CRYPT_XML_DATA_PROVIDER_READ","PFN_CRYPT_XML_DATA_PROVIDER_READ callback","PFN_CRYPT_XML_DATA_PROVIDER_READ callback function [Security]","cryptxml/PFN_CRYPT_XML_DATA_PROVIDER_READ","security.pfn_crypt_xml_data_provider_read"]
old-location: security\pfn_crypt_xml_data_provider_read.htm
tech.root: security
ms.assetid: 86c7003e-eee2-4adf-adf4-8f9d1acb5c45
ms.date: 12/05/2018
ms.keywords: PFN_CRYPT_XML_DATA_PROVIDER_READ, PFN_CRYPT_XML_DATA_PROVIDER_READ callback, PFN_CRYPT_XML_DATA_PROVIDER_READ callback function [Security], cryptxml/PFN_CRYPT_XML_DATA_PROVIDER_READ, security.pfn_crypt_xml_data_provider_read
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
 - PFN_CRYPT_XML_DATA_PROVIDER_READ
 - cryptxml/PFN_CRYPT_XML_DATA_PROVIDER_READ
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
 - PFN_CRYPT_XML_DATA_PROVIDER_READ
---

# PFN_CRYPT_XML_DATA_PROVIDER_READ callback function


## -description

The <i>PFN_CRYPT_XML_DATA_PROVIDER_READ</i> callback function reads XML data.

## -parameters

### -param pvCallbackState [in, out]

A pointer to an application defined argument that is passed to the calling function.

### -param pbData [out]

A pointer to the buffer that receives the data to be read.

### -param cbData [in]

The size, in bytes, of the data to be read.

### -param pcbRead [out]

A pointer to a variable that receives the number of bytes actually read.

## -returns

 The <i>PFN_CRYPT_XML_DATA_PROVIDER_READ</i> callback function returns a value when one of the 
    following conditions occurs:

<ul>
<li>A write operation completes on the data provider</li>
<li>The number of bytes requested is read</li>
<li>An error occurs</li>
</ul>
If the function succeeds, the function returns NO_ERROR.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.

If the value of <i>pcbRead</i> equals zero, then there is no more data available.

## -remarks

 The callback function does not return a value unless the number of bytes specified in <i>cbData</i> 
 is available or  the last block of data has been read.


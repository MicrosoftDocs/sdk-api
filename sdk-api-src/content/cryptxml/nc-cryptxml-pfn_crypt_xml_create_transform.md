---
UID: NC:cryptxml.PFN_CRYPT_XML_CREATE_TRANSFORM
title: PFN_CRYPT_XML_CREATE_TRANSFORM (cryptxml.h)
description: Creates a transform for a specified data provider.
helpviewer_keywords: ["PFN_CRYPT_XML_CREATE_TRANSFORM","PFN_CRYPT_XML_CREATE_TRANSFORM callback","PFN_CRYPT_XML_CREATE_TRANSFORM callback function [Security]","cryptxml/PFN_CRYPT_XML_CREATE_TRANSFORM","security.pfn_crypt_xml_create_transform"]
old-location: security\pfn_crypt_xml_create_transform.htm
tech.root: security
ms.assetid: d9228015-d5e7-4c72-9561-be4ee5fa4264
ms.date: 12/05/2018
ms.keywords: PFN_CRYPT_XML_CREATE_TRANSFORM, PFN_CRYPT_XML_CREATE_TRANSFORM callback, PFN_CRYPT_XML_CREATE_TRANSFORM callback function [Security], cryptxml/PFN_CRYPT_XML_CREATE_TRANSFORM, security.pfn_crypt_xml_create_transform
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
 - PFN_CRYPT_XML_CREATE_TRANSFORM
 - cryptxml/PFN_CRYPT_XML_CREATE_TRANSFORM
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
 - PFN_CRYPT_XML_CREATE_TRANSFORM
---

# PFN_CRYPT_XML_CREATE_TRANSFORM callback function


## -description

The  <i>PFN_CRYPT_XML_CREATE_TRANSFORM</i>  callback function creates a transform for a specified data provider.

## -parameters

### -param pTransform [in]

A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_algorithm">CRYPT_XML_ALGORITHM</a> structure that specifies the transform to apply.

### -param pProviderIn [in]

A pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_data_provider">CRYPT_XML_DATA_PROVIDER</a> structure that specifies the data provider to use as input for the transform.

### -param pProviderOut [out]

A pointer to a  <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_data_provider">CRYPT_XML_DATA_PROVIDER</a> structure to receive the data provider of the transform.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.

## -remarks

In the transform chain, the output of a transform is the input of the next transform in the chain.

 The implementation of the callback function is responsible for calling the  provider close function on the input transform to release the input provider.

---
UID: NC:cryptxml.PFN_CRYPT_XML_CREATE_TRANSFORM
title: PFN_CRYPT_XML_CREATE_TRANSFORM
author: windows-sdk-content
description: Creates a transform for a specified data provider.
old-location: security\pfn_crypt_xml_create_transform.htm
tech.root: SecCrypto
ms.assetid: d9228015-d5e7-4c72-9561-be4ee5fa4264
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PFN_CRYPT_XML_CREATE_TRANSFORM, PFN_CRYPT_XML_CREATE_TRANSFORM callback, PFN_CRYPT_XML_CREATE_TRANSFORM callback function [Security], cryptxml/PFN_CRYPT_XML_CREATE_TRANSFORM, security.pfn_crypt_xml_create_transform
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Cryptxml.h
api_name:
 - PFN_CRYPT_XML_CREATE_TRANSFORM
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CRYPT_XML_CREATE_TRANSFORM callback function


## -description


The  <i>PFN_CRYPT_XML_CREATE_TRANSFORM</i>  callback function creates a transform for a specified data provider.


## -parameters




### -param *pTransform [in]

A <a href="https://msdn.microsoft.com/4eb99c1e-fa06-41ec-906c-a3ba34e7aaeb">CRYPT_XML_ALGORITHM</a> structure that specifies the transform to apply.


### -param *pProviderIn [in]

A pointer to a <a href="https://msdn.microsoft.com/98f32310-a4fa-414c-8a3e-877839eacd1b">CRYPT_XML_DATA_PROVIDER</a> structure that specifies the data provider to use as input for the transform. 


### -param *pProviderOut [out]

A pointer to a  <a href="https://msdn.microsoft.com/98f32310-a4fa-414c-8a3e-877839eacd1b">CRYPT_XML_DATA_PROVIDER</a> structure to receive the data provider of the transform.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.




## -remarks



In the transform chain, the output of a transform is the input of the next transform in the chain.

 The implementation of the callback function is responsible for calling the  provider close function on the input transform to release the input provider.




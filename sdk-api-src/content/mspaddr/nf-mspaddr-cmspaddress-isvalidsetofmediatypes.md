---
UID: NF:mspaddr.CMSPAddress.IsValidSetOfMediaTypes
title: CMSPAddress::IsValidSetOfMediaTypes (mspaddr.h)
description: The IsValidSetOfMediaTypes method checks to see if the specified media type is nonzero and is in the specified mask.
helpviewer_keywords: ["CMSPAddress interface [TAPI 2.2]","IsValidSetOfMediaTypes method","CMSPAddress.IsValidSetOfMediaTypes","CMSPAddress::IsValidSetOfMediaTypes","IsValidSetOfMediaTypes","IsValidSetOfMediaTypes method [TAPI 2.2]","IsValidSetOfMediaTypes method [TAPI 2.2]","CMSPAddress interface","_tapi3_cmspaddress_isvalidsetofmediatypes","mspaddr/CMSPAddress::IsValidSetOfMediaTypes","tapi3.cmspaddress_isvalidsetofmediatypes"]
old-location: tapi3\cmspaddress_isvalidsetofmediatypes.htm
tech.root: tapi3
ms.assetid: 4dc47d60-184d-4601-8c58-08ae8b747223
ms.date: 12/05/2018
ms.keywords: CMSPAddress interface [TAPI 2.2],IsValidSetOfMediaTypes method, CMSPAddress.IsValidSetOfMediaTypes, CMSPAddress::IsValidSetOfMediaTypes, IsValidSetOfMediaTypes, IsValidSetOfMediaTypes method [TAPI 2.2], IsValidSetOfMediaTypes method [TAPI 2.2],CMSPAddress interface, _tapi3_cmspaddress_isvalidsetofmediatypes, mspaddr/CMSPAddress::IsValidSetOfMediaTypes, tapi3.cmspaddress_isvalidsetofmediatypes
req.header: mspaddr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - CMSPAddress::IsValidSetOfMediaTypes
 - mspaddr/CMSPAddress::IsValidSetOfMediaTypes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspaddr.h
api_name:
 - CMSPAddress.IsValidSetOfMediaTypes
---

# CMSPAddress::IsValidSetOfMediaTypes


## -description

The 
<b>IsValidSetOfMediaTypes</b> method checks to see if the specified media type is nonzero and is in the specified mask. Your MSP can override this if it needs to do atypically complex checks on specific combinations of media types (for example, can never have more than one media type on a call, can have video with audio but not video alone, and so on). The default implementation accepts any nonempty set of media types that is a subset of the set of types in the mask.

## -parameters

### -param dwMediaType [in]

<a href="/windows/desktop/Tapi/tapimediatype--constants">Media type</a> to check.

### -param dwMask [in]

Media types mask indicating types that can be handled.

## -see-also

<a href="/windows/desktop/api/mspaddr/nl-mspaddr-cmspaddress">CMSPAddress</a>
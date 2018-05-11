---
UID: NF:mspaddr.CMSPAddress.IsValidSetOfMediaTypes
title: CMSPAddress::IsValidSetOfMediaTypes
author: windows-driver-content
description: The IsValidSetOfMediaTypes method checks to see if the specified media type is nonzero and is in the specified mask.
old-location: tapi3\cmspaddress_isvalidsetofmediatypes.htm
old-project: Tapi
ms.assetid: 4dc47d60-184d-4601-8c58-08ae8b747223
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: CMSPAddress interface [TAPI 2.2],IsValidSetOfMediaTypes method, CMSPAddress.IsValidSetOfMediaTypes, CMSPAddress::IsValidSetOfMediaTypes, IsValidSetOfMediaTypes, IsValidSetOfMediaTypes method [TAPI 2.2], IsValidSetOfMediaTypes method [TAPI 2.2],CMSPAddress interface, _tapi3_cmspaddress_isvalidsetofmediatypes, mspaddr/CMSPAddress::IsValidSetOfMediaTypes, tapi3.cmspaddress_isvalidsetofmediatypes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MSP_EVENT_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mspaddr.h
api_name:
-	CMSPAddress.IsValidSetOfMediaTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CMSPAddress::IsValidSetOfMediaTypes


## -description


The 
<b>IsValidSetOfMediaTypes</b> method checks to see if the specified media type is nonzero and is in the specified mask. Your MSP can override this if it needs to do atypically complex checks on specific combinations of media types (for example, can never have more than one media type on a call, can have video with audio but not video alone, and so on). The default implementation accepts any nonempty set of media types that is a subset of the set of types in the mask.


## -parameters




### -param dwMediaType [in]


<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">Media type</a> to check.


### -param dwMask [in]

Media types mask indicating types that can be handled.


## -see-also




<a href="https://msdn.microsoft.com/864bf814-43dd-4d2b-a5a7-fff12520accb">CMSPAddress</a>
 

 


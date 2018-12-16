---
UID: NF:encdec.IETFilter.GetCurrRating
title: IETFilter::GetCurrRating
author: windows-sdk-content
description: The GetCurrRating method retrieves the current rating, based on the most recent media sample.
old-location: mstv\ietfilter_getcurrrating.htm
tech.root: mstv
ms.assetid: d90d0842-2dd3-4b98-b619-1b71f7870be8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCurrRating, GetCurrRating method [Microsoft TV Technologies], GetCurrRating method [Microsoft TV Technologies],IETFilter interface, IETFilter interface [Microsoft TV Technologies],GetCurrRating method, IETFilter.GetCurrRating, IETFilter::GetCurrRating, IETFilterGetCurrRating, encdec/IETFilter::GetCurrRating, mstv.ietfilter_getcurrrating
ms.topic: method
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
 - COM
api_location:
 - EncDec.h
api_name:
 - IETFilter.GetCurrRating
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IETFilter::GetCurrRating


## -description


The <b>GetCurrRating</b> method retrieves the current rating, based on the most recent media sample.


## -parameters




### -param pEnSystem [out]

Receives the rating system, as an <a href="https://msdn.microsoft.com/646927ad-569a-4484-a3ce-6d121210b6be">EnTvRat_System</a> enumeration type.


### -param pEnRating [out]

Receives the rating level, as an <a href="https://msdn.microsoft.com/f96a8f1a-d8e2-4976-92e3-719f0039d2a8">EnTvRat_GenericLevel</a> enumeration type. The meaning of this value depends on the rating system.


### -param plbfEnAttr [out]

Receives a bitwise combination of flags from the <a href="https://msdn.microsoft.com/eb7f56c4-1d48-43f9-a691-c08aee3cd537">BfEnTvRat_GenericAttributes</a> enumeration. The flags specify content attributes, such as violence or adult language. Content attributes do not apply to all rating systems.


## -returns



Returns S_OK if successful, or an error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/9fce6b33-394c-47d2-9d02-7b0dadaa1736">IETFilter Interface</a>
 

 


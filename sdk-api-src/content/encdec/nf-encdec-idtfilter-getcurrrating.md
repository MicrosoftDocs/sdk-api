---
UID: NF:encdec.IDTFilter.GetCurrRating
title: IDTFilter::GetCurrRating
author: windows-driver-content
description: The GetCurrRating method retrieves the current rating, based on the most recent media sample.
old-location: mstv\idtfilter_getcurrrating.htm
old-project: mstv
ms.assetid: 6ea5c9a0-b04c-41a6-83ed-48ea9d187da7
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetCurrRating, GetCurrRating method [Microsoft TV Technologies], GetCurrRating method [Microsoft TV Technologies],IDTFilter interface, IDTFilter interface [Microsoft TV Technologies],GetCurrRating method, IDTFilter.GetCurrRating, IDTFilter::GetCurrRating, IDTFilterGetCurrRating, encdec/IDTFilter::GetCurrRating, mstv.idtfilter_getcurrrating
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ProtType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EncDec.h
api_name:
-	IDTFilter.GetCurrRating
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDTFilter::GetCurrRating


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




<a href="https://msdn.microsoft.com/15acf764-7e4d-40c3-b907-ff5dfaa69dae">IDTFilter Interface</a>
 

 


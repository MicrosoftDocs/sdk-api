---
UID: NN:tvratings.IEvalRat
title: IEvalRat
author: windows-sdk-content
description: The IEvalRat interface is used to evaluate content ratings carried by a broadcast stream.
old-location: mstv\ievalrat.htm
old-project: mstv
ms.assetid: b37c7e7d-80fd-4a42-a698-c20ffb2a5052
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IEvalRat, IEvalRat interface [Microsoft TV Technologies], IEvalRat interface [Microsoft TV Technologies],described, IEvalRatInterface, mstv.ievalrat, tvratings/IEvalRat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tvratings.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EnTvRat_US_TV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tvratings.h
api_name:
 - IEvalRat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEvalRat interface


## -description



The <b>IEvalRat</b> interface is used to evaluate content ratings carried by a broadcast stream. This interface is exposed by the <a href="https://msdn.microsoft.com/6a67cdb1-9a5c-4130-a29c-05c584702fd9">EvalRat</a> (ratings evaluator) object. The EvalRat object is implemented by third parties.

The Encrypter/Tagger filter and the Decrypter/Detagger filter use this interface. Applications use the interfaces exposed by those filters, but typically do not use the <b>IEvalRat</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEvalRat</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IEvalRat</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEvalRat</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d07b6462-958c-4e97-9be1-41941aa6b747">get_BlockedRatingAttributes</a>
</td>
<td align="left" width="63%">
Determines whether content is blocked for a given rating system and rating level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f558c87e-59ac-40d3-bfab-2835d59a730b">get_BlockUnRated</a>
</td>
<td align="left" width="63%">
Indicates whether a program without rating information is blocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b744715f-53a8-4011-9657-d2962f0e7f6e">MostRestrictiveRating</a>
</td>
<td align="left" width="63%">
Compares two ratings and returns the more restrictive of the two.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c6919f0-1270-4dcd-8180-a9af4763c580">put_BlockedRatingAttributes</a>
</td>
<td align="left" width="63%">
Specifies whether to block content that has a specified rating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22f6bc32-3f41-45d4-83e5-f501cbeb772e">put_BlockUnRated</a>
</td>
<td align="left" width="63%">
Specifies whether to block a program for which rating information has not been obtained.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26144496-200c-49b8-9f5e-23a39fea20bc">TestRating</a>
</td>
<td align="left" width="63%">
Determines whether a program with the specified rating should be blocked.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEvalRat)</code>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/abe939a3-5f43-4fdf-9d4d-34b7be8893eb">TV Ratings Interfaces</a>
 

 


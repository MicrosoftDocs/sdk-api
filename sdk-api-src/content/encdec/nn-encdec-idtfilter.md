---
UID: NN:encdec.IDTFilter
title: IDTFilter
author: windows-sdk-content
description: The IDTFilter interface is exposed by the Decrypter/Detagger filter. Applications can use this interface to set the ratings permissions.
old-location: mstv\idtfilter.htm
old-project: mstv
ms.assetid: 15acf764-7e4d-40c3-b907-ff5dfaa69dae
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDTFilter, IDTFilter interface [Microsoft TV Technologies], IDTFilter interface [Microsoft TV Technologies],described, IDTFilterInterface, encdec/IDTFilter, mstv.idtfilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: ProtType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EncDec.h
api_name:
-	IDTFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDTFilter interface


## -description



The <b>IDTFilter</b> interface is exposed by the Decrypter/Detagger filter. Applications can use this interface to set the ratings permissions.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDTFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDTFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDTFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf7a5596-3d10-4ce9-a8c8-2703cf1eb7f8">get_BlockedRatingAttributes</a>
</td>
<td align="left" width="63%">
Determines whether content is blocked for a given rating system and rating level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b8ecc6b-02e8-47e9-a8df-6e73d58dd177">get_BlockUnRated</a>
</td>
<td align="left" width="63%">
Indicates whether a program without rating information is blocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6852f376-35ab-4628-9068-51a2ca2ea31f">get_BlockUnRatedDelay</a>
</td>
<td align="left" width="63%">
Retrieves that length of time the filter waits before it blocks unrated content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92bbe476-3aba-4a50-9cb3-500356228c4b">get_EvalRatObjOK</a>
</td>
<td align="left" width="63%">
Queries whether the <a href="https://msdn.microsoft.com/6a67cdb1-9a5c-4130-a29c-05c584702fd9">EvalRat</a> object was created successfully.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ea5c9a0-b04c-41a6-83ed-48ea9d187da7">GetCurrRating</a>
</td>
<td align="left" width="63%">
Retrieves the current rating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae81e427-305e-43b8-ad4d-e23f0bbbdc4a">put_BlockedRatingAttributes</a>
</td>
<td align="left" width="63%">
Specifies whether to block content that has a specified rating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b6ef516-bbc8-4d17-a306-433e8265e879">put_BlockUnRated</a>
</td>
<td align="left" width="63%">
Specifies whether to block a program for which rating information has not been obtained.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2caabce8-57b0-4a43-87b7-1b045ca573db">put_BlockUnRatedDelay</a>
</td>
<td align="left" width="63%">
Sets the length of time the filter waits before it blocks unrated content.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDTFilter)</code>.




## -see-also




<a href="https://msdn.microsoft.com/abe939a3-5f43-4fdf-9d4d-34b7be8893eb">TV Ratings Interfaces</a>
 

 


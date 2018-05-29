---
UID: NN:tvratings.IXDSToRat
title: IXDSToRat
author: windows-sdk-content
description: The IXDSToRat interface parses rating information from extended data services (XDS) information in line 21.
old-location: mstv\ixdstorat.htm
old-project: mstv
ms.assetid: de65e5cd-3f4b-4925-a6b8-636fc2e332ec
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IXDSToRat, IXDSToRat interface [Microsoft TV Technologies], IXDSToRat interface [Microsoft TV Technologies],described, IXDSToRatInterface, mstv.ixdstorat, tvratings/IXDSToRat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tvratings.h
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
req.typenames: EnTvRat_US_TV
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tvratings.h
api_name:
-	IXDSToRat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IXDSToRat interface


## -description



The <b>IXDSToRat</b> interface parses rating information from extended data services (XDS) information in line 21. This interface is exposed by the <a href="https://msdn.microsoft.com/bda34c12-0eb8-4d3a-867e-f7215f70c7c7">XDSToRat</a> (ratings decoder) object. The XDSToRat object is implemented by third parties.

The XDS Codec filter uses this interface. Applications do not use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXDSToRat</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IXDSToRat</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXDSToRat</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/bda34c12-0eb8-4d3a-867e-f7215f70c7c7">XDSToRat</a> object to its initial state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79c83962-13ac-4604-a6f0-677ea6f4af84">ParseXDSBytePair</a>
</td>
<td align="left" width="63%">
Parses a single byte pair from an XDS stream.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IXDSToRat)</code>.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/abe939a3-5f43-4fdf-9d4d-34b7be8893eb">TV Ratings Interfaces</a>
 

 


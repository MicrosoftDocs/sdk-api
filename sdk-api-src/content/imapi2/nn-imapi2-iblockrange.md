---
UID: NN:imapi2.IBlockRange
title: IBlockRange
author: windows-sdk-content
description: Use this interface to retrieve information about a single continuous range of sectors on the media. This interface is typically used together with the IBlockRangeList interface to describe a collection of sector ranges.
old-location: imapi\iblockrange.htm
tech.root: imapi
ms.assetid: abebc651-0575-4b76-9fe8-2cea3d617582
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IBlockRange, IBlockRange interface [IMAPI], IBlockRange interface [IMAPI],described, imapi.iblockrange, imapi2/IBlockRange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IBlockRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBlockRange interface


## -description


Use this interface to retrieve information about a single continuous range of sectors on the media. This interface is typically used together with the <a href="https://msdn.microsoft.com/f2a3bd54-4f40-4bf0-9cbf-b507819d669f">IBlockRangeList</a> interface to describe a collection of sector ranges.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBlockRange</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IBlockRange</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBlockRange</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2260241-5922-4cf5-8aff-1dd7431a44c2">get_EndLba</a>
</td>
<td align="left" width="63%">
Retrieves the end sector in the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6891aebd-3795-4e1c-a065-1579a984de41">get_StartLba</a>
</td>
<td align="left" width="63%">
Retrieves the start sector in the range.

</td>
</tr>
</table> 


## -remarks



The values returned by the <a href="https://msdn.microsoft.com/6891aebd-3795-4e1c-a065-1579a984de41">IBlockRange::get_StartLba</a> and <a href="https://msdn.microsoft.com/e2260241-5922-4cf5-8aff-1dd7431a44c2">IBlockRange::get_EndLba</a> methods define an inclusive range, i.e. both the start and end sectors belong to the range.




## -see-also




<a href="https://msdn.microsoft.com/f2a3bd54-4f40-4bf0-9cbf-b507819d669f">IBlockRangeList</a>



<a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 


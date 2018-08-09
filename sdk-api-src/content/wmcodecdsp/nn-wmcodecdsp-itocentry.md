---
UID: NN:wmcodecdsp.ITocEntry
title: ITocEntry
author: windows-sdk-content
description: The ITocEntry interface represents an individual entry in a table of contents. It provides methods for setting and retrieving descriptive information for the entry.
old-location: mf\itocentry.htm
old-project: medfound
ms.assetid: 82a1a390-50b1-4699-9baa-60cea322ce7c
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ITocEntry, ITocEntry interface [Media Foundation], ITocEntry interface [Media Foundation],described, codecapi.itocentry, mf.itocentry, wmcodecdsp/ITocEntry
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFVideoDSPMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmvdspa.dll
api_name:
 - ITocEntry
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ITocEntry interface


## -description


The <b>ITocEntry</b> interface represents an individual entry in a table of contents. It provides methods for setting and retrieving descriptive information for the entry.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITocEntry</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITocEntry</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITocEntry</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4000b67c-e34e-4bce-9a0d-c56c9fc0f41e">GetDescriptionData</a>
</td>
<td align="left" width="63%">
Gets a description data block that was previously associated with the entry by a call to <a href="https://msdn.microsoft.com/260d7699-cf75-4179-9f2b-bc3bc49c94e6">SetDescriptionData</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439771">GetDescriptor</a>
</td>
<td align="left" width="63%">
Gets the descriptor, previously set by a call to <a href="https://msdn.microsoft.com/09a366a6-fcb4-4a0b-8df1-795360d147b9">SetDescriptor</a>, of the entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/583340d7-87f9-40c5-a0dc-3e69bbb96334">GetSubEntries</a>
</td>
<td align="left" width="63%">
Gets an array of subentry indices that were set by a previous call to <a href="https://msdn.microsoft.com/4b3f4038-483c-4f00-a819-ace83d99da58">SetSubEntries</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d610e9e8-daa4-4d8c-a640-627b23afd316">GetTitle</a>
</td>
<td align="left" width="63%">
 Gets the title, set by a previous call to <a href="https://msdn.microsoft.com/24ab6c56-59ae-4fdf-b18e-75f616ee5a80">SetTitle</a>, of the entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/260d7699-cf75-4179-9f2b-bc3bc49c94e6">SetDescriptionData</a>
</td>
<td align="left" width="63%">
Associates a caller-supplied data block with the entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09a366a6-fcb4-4a0b-8df1-795360d147b9">SetDescriptor</a>
</td>
<td align="left" width="63%">
Associates a descriptor with the entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b3f4038-483c-4f00-a819-ace83d99da58">SetSubEntries</a>
</td>
<td align="left" width="63%">
Identifies a set of entries as being subentries of this entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24ab6c56-59ae-4fdf-b18e-75f616ee5a80">SetTitle</a>
</td>
<td align="left" width="63%">
Sets the title of the entry.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/25039e6c-dd2a-4516-bf27-8e9d6ca0f00e">Table of Contents Parser Interfaces</a>
 

 


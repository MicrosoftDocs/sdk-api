---
UID: NN:wmcodecdsp.IToc
title: IToc (wmcodecdsp.h)
author: windows-sdk-content
description: The IToc interface represents an individual table of contents. It provides methods for adding entries to, and removing entries from the table of contents.
old-location: mf\itoc.htm
tech.root: medfound
ms.assetid: b12d38c7-b80e-4ca8-9ac5-a116100911d0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IToc, IToc interface [Media Foundation], IToc interface [Media Foundation],described, codecapi.itoc, mf.itoc, wmcodecdsp/IToc
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
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmvdspa.dll
api_name:
 - IToc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IToc interface


## -description


The <b>IToc</b> interface represents an individual table of contents. It provides methods for adding  entries to, and removing entries from the table of contents.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IToc</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IToc</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IToc</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylist">AddEntryList</a>
</td>
<td align="left" width="63%">
Adds an entry list to the table of contents and assigns an index to the entry list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ee264281(v%3dvs.85)">AddEntryListByIndex</a>
</td>
<td align="left" width="63%">
Adds an entry list to the table of contents and associates a caller-supplied index with the entry list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getcontext">GetContext</a>
</td>
<td align="left" width="63%">
Retrieves a block of bytes that was previously associated with the table of contents by a call to <a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-setcontext">SetContext</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description, set by a previous call to <a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-setdescription">SetDescription</a>, of the table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getdescriptor">GetDescriptor</a>
</td>
<td align="left" width="63%">
Retrieves the descriptor, previously set by <a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-setdescriptor">SetDescriptor</a>, of the table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ee264285(v%3dvs.85)">GetEntryListByIndex</a>
</td>
<td align="left" width="63%">
Retrieves an entry list, specified by an index, from the table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistcount">GetEntryListCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of entry lists in the table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ee264287(v%3dvs.85)">RemoveEntryListByIndex</a>
</td>
<td align="left" width="63%">
Removes an entry list, specified by an index, from the table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-setcontext">SetContext</a>
</td>
<td align="left" width="63%">
Associates a caller-supplied context block with the table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-setdescription">SetDescription</a>
</td>
<td align="left" width="63%">
Associates a description with the table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-setdescriptor">SetDescriptor</a>
</td>
<td align="left" width="63%">
Associates a descriptor with the table of contents.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/toc-parser-interfaces">Table of Contents Parser Interfaces</a>
 

 


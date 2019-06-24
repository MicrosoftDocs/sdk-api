---
UID: NN:wmcodecdsp.ITocEntryList
title: ITocEntryList (wmcodecdsp.h)
author: windows-sdk-content
description: The ITocEntryList interface represents a list of entries in a table of contents. It provides methods for adding entries to, and removing entries from the list.
old-location: mf\itocentrylist.htm
tech.root: medfound
ms.assetid: 98052f26-7956-4973-ab86-428e7a355937
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITocEntryList, ITocEntryList interface [Media Foundation], ITocEntryList interface [Media Foundation],described, codecapi.itocentrylist, mf.itocentrylist, wmcodecdsp/ITocEntryList
ms.topic: interface
f1_keywords: ["wmcodecdsp/ITocEntryList"]
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
 - ITocEntryList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITocEntryList interface


## -description


The <b>ITocEntryList</b> interface represents a list of entries in a table of contents. It provides methods for adding entries to, and removing entries from the list.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITocEntryList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITocEntryList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITocEntryList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentry">AddEntry</a>
</td>
<td align="left" width="63%">
Adds an individual entry to the list and assigns an index to the entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ee264259(v=vs.85)">AddEntryByIndex</a>
</td>
<td align="left" width="63%">
Adds an individual entry to the list and associates a caller-supplied index with the entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex">GetEntryByIndex</a>
</td>
<td align="left" width="63%">
Retrieves an entry, specified by an index, from the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrycount">GetEntryCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of entries in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ee264262(v=vs.85)">RemoveEntryByIndex</a>
</td>
<td align="left" width="63%">
Removes an entry, specified by an index, from the list.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/toc-parser-interfaces">Table of Contents Parser Interfaces</a>
 

 


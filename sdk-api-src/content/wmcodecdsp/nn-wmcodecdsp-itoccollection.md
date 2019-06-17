---
UID: NN:wmcodecdsp.ITocCollection
title: ITocCollection (wmcodecdsp.h)
author: windows-sdk-content
description: The ITocCollection represents a collection of tables of contents. It provides methods for adding, retrieving, and removing, tables of contents from the collection.
old-location: mf\itoccollection.htm
tech.root: medfound
ms.assetid: 10d6fc04-4444-4a47-911f-3d5bec548e28
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITocCollection, ITocCollection interface [Media Foundation], ITocCollection interface [Media Foundation],described, codecapi.itoccollection, mf.itoccollection, wmcodecdsp/ITocCollection
ms.topic: interface
f1_keywords: ["wmcodecdsp/ITocCollection"]
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
 - ITocCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITocCollection interface


## -description


The <b>ITocCollection</b> represents a collection of tables of contents. It provides methods for adding, retrieving, and removing,  tables of contents from the collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITocCollection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITocCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITocCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoccollection-addentry">AddEntry</a>
</td>
<td align="left" width="63%">
Adds an individual table of contents  to the collection, and assigns an index to the added table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ee264252(v%3dvs.85)">AddEntryByIndex</a>
</td>
<td align="left" width="63%">
Adds an individual table of contents to the collection, and associates a caller-supplied index with that table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ee264253(v%3dvs.85)">GetEntryByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a table of contents, specified by an index, from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoccollection-getentrycount">GetEntryCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of tables of contents in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ee264255(v%3dvs.85)">RemoveEntryByIndex</a>
</td>
<td align="left" width="63%">
 Removes a table of contents, specified by an index, from  the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/toc-parser-interfaces">Table of Contents Parser Interfaces</a>
 

 


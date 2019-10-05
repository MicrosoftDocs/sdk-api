---
UID: NN:wmcodecdsp.ITocParser
title: ITocParser (wmcodecdsp.h)
author: windows-sdk-content
description: The ITocParser interface represents a TOC Parser object. It provides methods for storing tables of contents in a video file and retrieving tables of contents from a video file.
old-location: mf\itocparser.htm
tech.root: medfound
ms.assetid: d1f14a6e-d75c-4266-beff-0e9af911edfe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITocParser, ITocParser interface [Media Foundation], ITocParser interface [Media Foundation],described, codecapi.itocparser, mf.itocparser, wmcodecdsp/ITocParser
ms.topic: interface
f1_keywords: 
 - "wmcodecdsp/ITocParser"
dev_langs:
 - c++
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
 - ITocParser
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITocParser interface


## -description


The <b>ITocParser</b> interface represents a TOC Parser object. It provides methods for storing tables of contents in a video file and retrieving tables of contents from a video file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITocParser</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITocParser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITocParser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc">AddToc</a>
</td>
<td align="left" width="63%">
Adds a table of contents to the TOC Parser object and assigns an index to the added table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit">Commit</a>
</td>
<td align="left" width="63%">
Stores the current state of the TOC Parser object in its associated media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex">GetTocByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a table of contents, specified by an index, from the TOC Parser object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype">GetTocByType</a>
</td>
<td align="left" width="63%">
Retrieves all tables of contents of a specified type from the TOC Parser object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount">GetTocCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of tables of contents, of a specified <a href="https://docs.microsoft.com/windows/desktop/medfound/the-position-type-of-a-table-of-contents">position type</a>, in the TOC Parser object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init">Init</a>
</td>
<td align="left" width="63%">
 Initializes the TOC Parser object and associates it with a media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ee264278(v=vs.85)">RemoveTocByIndex</a>
</td>
<td align="left" width="63%">
Removes a table of contents, specified by an index, from the TOC Parser object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype">RemoveTocByType</a>
</td>
<td align="left" width="63%">
Removes all tables of contents of a specified type from the TOC Parser object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/toc-parser-interfaces">Table of Contents Parser Interfaces</a>
 

 


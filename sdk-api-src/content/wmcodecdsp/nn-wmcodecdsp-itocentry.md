---
UID: NN:wmcodecdsp.ITocEntry
title: ITocEntry (wmcodecdsp.h)

description: The ITocEntry interface represents an individual entry in a table of contents. It provides methods for setting and retrieving descriptive information for the entry.
old-location: mf\itocentry.htm
tech.root: medfound
ms.assetid: 82a1a390-50b1-4699-9baa-60cea322ce7c

ms.date: 12/05/2018
ms.keywords: ITocEntry, ITocEntry interface [Media Foundation], ITocEntry interface [Media Foundation],described, codecapi.itocentry, mf.itocentry, wmcodecdsp/ITocEntry
ms.topic: interface
f1_keywords: 
 - "wmcodecdsp/ITocEntry"
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
 - ITocEntry
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITocEntry interface


## -description


The <b>ITocEntry</b> interface represents an individual entry in a table of contents. It provides methods for setting and retrieving descriptive information for the entry.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITocEntry</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITocEntry</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptiondata">GetDescriptionData</a>
</td>
<td align="left" width="63%">
Gets a description data block that was previously associated with the entry by a call to <a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptiondata">SetDescriptionData</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor">GetDescriptor</a>
</td>
<td align="left" width="63%">
Gets the descriptor, previously set by a call to <a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor">SetDescriptor</a>, of the entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getsubentries">GetSubEntries</a>
</td>
<td align="left" width="63%">
Gets an array of subentry indices that were set by a previous call to <a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setsubentries">SetSubEntries</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-gettitle">GetTitle</a>
</td>
<td align="left" width="63%">
 Gets the title, set by a previous call to <a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-settitle">SetTitle</a>, of the entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptiondata">SetDescriptionData</a>
</td>
<td align="left" width="63%">
Associates a caller-supplied data block with the entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor">SetDescriptor</a>
</td>
<td align="left" width="63%">
Associates a descriptor with the entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setsubentries">SetSubEntries</a>
</td>
<td align="left" width="63%">
Identifies a set of entries as being subentries of this entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-settitle">SetTitle</a>
</td>
<td align="left" width="63%">
Sets the title of the entry.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/toc-parser-interfaces">Table of Contents Parser Interfaces</a>
 

 


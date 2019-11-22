---
UID: NN:mpeg2data.IMpeg2TableFilter
title: IMpeg2TableFilter (mpeg2data.h)

description: The IMpeg2TableFilter interface controls which tables are parsed by the MPEG-2 Sections and Tables filter. The BDA MPEG-2 Transport Information filter exposes this interface on its output pins.
old-location: mstv\impeg2tablefilter.htm
tech.root: mstv
ms.assetid: 9467352d-44a5-41eb-b426-28df83a6d423

ms.date: 12/05/2018
ms.keywords: IMpeg2TableFilter, IMpeg2TableFilter interface [Microsoft TV Technologies], IMpeg2TableFilter interface [Microsoft TV Technologies],described, IMpeg2TableFilterInterface, mpeg2data/IMpeg2TableFilter, mstv.impeg2tablefilter
ms.topic: interface
f1_keywords: 
 - "mpeg2data/IMpeg2TableFilter"
dev_langs:
 - c++
req.header: mpeg2data.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2data.h
api_name:
 - IMpeg2TableFilter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMpeg2TableFilter interface


## -description



The <b>IMpeg2TableFilter</b> interface controls which tables are parsed by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/mpeg-2-sections-and-tables-filter">MPEG-2 Sections and Tables</a> filter. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information</a> filter exposes this interface on its output pins.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMpeg2TableFilter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMpeg2TableFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMpeg2TableFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2tablefilter-addextension">AddExtension</a>
</td>
<td align="left" width="63%">
Adds a table extension to the list of MPEG-2 table sections that the filter sends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2tablefilter-addpid">AddPID</a>
</td>
<td align="left" width="63%">
Adds a packet identifier (PID) to the list of PIDs that the filter sends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2tablefilter-addtable">AddTable</a>
</td>
<td align="left" width="63%">
Adds a table identifier (TID) to the list of MPEG-2 table sections that the filter sends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2tablefilter-removeextension">RemoveExtension</a>
</td>
<td align="left" width="63%">
Removes a table extension from the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2tablefilter-removepid">RemovePID</a>
</td>
<td align="left" width="63%">
Removes a PID from the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2tablefilter-removetable">RemoveTable</a>
</td>
<td align="left" width="63%">
Removes a TID from the list.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMpeg2TableFilter)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/mpeg-2-sections-and-tables-filter">MPEG-2 Sections and Tables Filter</a>
 

 


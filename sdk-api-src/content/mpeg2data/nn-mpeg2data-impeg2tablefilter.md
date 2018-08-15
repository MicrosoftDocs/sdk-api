---
UID: NN:mpeg2data.IMpeg2TableFilter
title: IMpeg2TableFilter
author: windows-sdk-content
description: The IMpeg2TableFilter interface controls which tables are parsed by the MPEG-2 Sections and Tables filter. The BDA MPEG-2 Transport Information filter exposes this interface on its output pins.
old-location: mstv\impeg2tablefilter.htm
old-project: mstv
ms.assetid: 9467352d-44a5-41eb-b426-28df83a6d423
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMpeg2TableFilter, IMpeg2TableFilter interface [Microsoft TV Technologies], IMpeg2TableFilter interface [Microsoft TV Technologies],described, IMpeg2TableFilterInterface, mpeg2data/IMpeg2TableFilter, mstv.impeg2tablefilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mpeg2data.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2data.h
api_name:
 - IMpeg2TableFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMpeg2TableFilter interface


## -description



The <b>IMpeg2TableFilter</b> interface controls which tables are parsed by the <a href="https://msdn.microsoft.com/03027748-03da-485c-8787-3cf171fff1e0">MPEG-2 Sections and Tables</a> filter. The <a href="https://msdn.microsoft.com/22044a4c-480f-4c98-a78e-52c66a5eac99">BDA MPEG-2 Transport Information</a> filter exposes this interface on its output pins.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMpeg2TableFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMpeg2TableFilter</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/20484b0e-c6c8-4741-9672-a991ba368e92">AddExtension</a>
</td>
<td align="left" width="63%">
Adds a table extension to the list of MPEG-2 table sections that the filter sends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a811d1f-cb1b-4f45-8dee-ba83efd20709">AddPID</a>
</td>
<td align="left" width="63%">
Adds a packet identifier (PID) to the list of PIDs that the filter sends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b789bfda-bb7e-4a7b-999e-0e2e798df4d5">AddTable</a>
</td>
<td align="left" width="63%">
Adds a table identifier (TID) to the list of MPEG-2 table sections that the filter sends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f29f29d-d411-44b7-bedb-6d10c49a0d4d">RemoveExtension</a>
</td>
<td align="left" width="63%">
Removes a table extension from the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9ce49e3-e256-4150-ab73-b57ed34ab30c">RemovePID</a>
</td>
<td align="left" width="63%">
Removes a PID from the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8875340-48cf-47eb-a7cc-58e181df37fb">RemoveTable</a>
</td>
<td align="left" width="63%">
Removes a TID from the list.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMpeg2TableFilter)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>



<a href="https://msdn.microsoft.com/22044a4c-480f-4c98-a78e-52c66a5eac99">BDA MPEG-2 Transport Information Filter</a>



<a href="https://msdn.microsoft.com/03027748-03da-485c-8787-3cf171fff1e0">MPEG-2 Sections and Tables Filter</a>
 

 


---
UID: NN:mpeg2data.IMpeg2Data
title: IMpeg2Data
author: windows-sdk-content
description: IMpeg2Data is no longer available for use as of Windows 7.
old-location: mstv\impeg2data.htm
old-project: mstv
ms.assetid: 82af47a2-cac4-4d4f-ba20-d4f6b5485a65
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMpeg2Data, IMpeg2Data interface [Microsoft TV Technologies], IMpeg2Data interface [Microsoft TV Technologies],described, IMpeg2DataInterface, mpeg2data/IMpeg2Data, mstv.impeg2data
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mpeg2data.h
api_name:
-	IMpeg2Data
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMpeg2Data interface


## -description


<p class="CCE_Message">[<b>IMpeg2Data</b> is no longer available for use as of Windows 7. Instead, use the <a href="https://msdn.microsoft.com/6f07b4d2-7a52-448c-9e9f-729bd5261757">IPSITables</a> interface to get program specific information (PSI) tables from an MPEG-2 transport stream.]

The <b>IMpeg2Data</b> interface is exposed by the <a href="https://msdn.microsoft.com/03027748-03da-485c-8787-3cf171fff1e0">MPEG-2 Sections and Tables</a> filter. It enables the client to retrieve unparsed sections or tables from an MPEG-2 transport stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMpeg2Data</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMpeg2Data</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMpeg2Data</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9fb0d10f-7f9a-452d-9725-546d372430bd">GetSection</a>
</td>
<td align="left" width="63%">
Retrieves an MPEG-2 table section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/896080ff-cdf0-40b1-ba4e-d94de527d86e">GetStreamOfSections</a>
</td>
<td align="left" width="63%">
Starts an ongoing request for specific MPEG-2 table sections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c76a9117-5dd7-46fc-8390-3f1ec80f6499">GetTable</a>
</td>
<td align="left" width="63%">
Retrieves a complete MPEG-2 PSI table.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMpeg2Data)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>



<a href="https://msdn.microsoft.com/e75ef5c2-7316-4f23-b108-ff16cd97622f">Getting MPEG-2 PSI Tables</a>
 

 


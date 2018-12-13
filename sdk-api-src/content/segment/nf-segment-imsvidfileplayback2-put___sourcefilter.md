---
UID: NF:segment.IMSVidFilePlayback2.put___SourceFilter
title: IMSVidFilePlayback2::put___SourceFilter
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
old-location: mstv\imsvidfileplayback2_put___sourcefilter.htm
tech.root: mstv
ms.assetid: 257e93ec-fb26-45fb-b07b-4491dbf2528a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidFilePlayback2 interface [Microsoft TV Technologies],put___SourceFilter method, IMSVidFilePlayback2.put___SourceFilter, IMSVidFilePlayback2::put___SourceFilter, IMSVidFilePlayback2put___SourceFilter, mstv.imsvidfileplayback2_put___sourcefilter, put___SourceFilter, put___SourceFilter method [Microsoft TV Technologies], put___SourceFilter method [Microsoft TV Technologies],IMSVidFilePlayback2 interface, segment/IMSVidFilePlayback2::put___SourceFilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - segment.h
api_name:
 - IMSVidFilePlayback2.put___SourceFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidFilePlayback2::put___SourceFilter


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
        



The <b>put___SourceFilter</b> method sets the CLSID of a DirectShow source filter to use for this source.


## -parameters




### -param FileName [in]

Specifies the CLSID of the source filter.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



If the CLSID is GUID_NULL, the <a href="https://msdn.microsoft.com/da8a1d86-b3a5-4488-8bbc-82dd09aeeaca">MSVidFilePlaybackDevice</a> object uses the default source filter for the file name given in <a href="https://msdn.microsoft.com/1055a053-28d3-470f-aff5-ade71eebc809">IMSVidFilePlayback::put_FileName</a>.




## -see-also




<a href="https://msdn.microsoft.com/5779d5f8-74b1-4318-9fda-1dae3bf4a3f5">IMSVidFilePlayback2 Interface</a>
 

 


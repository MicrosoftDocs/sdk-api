---
UID: NF:segment.IMSVidFilePlayback2.put__SourceFilter
title: IMSVidFilePlayback2::put__SourceFilter
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
old-location: mstv\imsvidfileplayback2_put__sourcefilter.htm
old-project: mstv
ms.assetid: ef536087-dd2b-417f-b139-916d930e3d25
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidFilePlayback2 interface [Microsoft TV Technologies],put__SourceFilter method, IMSVidFilePlayback2.put__SourceFilter, IMSVidFilePlayback2::put__SourceFilter, IMSVidFilePlayback2put__SourceFilter, mstv.imsvidfileplayback2_put__sourcefilter, put__SourceFilter, put__SourceFilter method [Microsoft TV Technologies], put__SourceFilter method [Microsoft TV Technologies],IMSVidFilePlayback2 interface, segment/IMSVidFilePlayback2::put__SourceFilter
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidFilePlayback2.put__SourceFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidFilePlayback2::put__SourceFilter


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
        



The <b>put__SourceFilter</b> method sets the CLSID of a DirectShow source filter to use for this source. The CLSID is specified as a string.


## -parameters




### -param FileName [in]

<b>BSTR</b> that contains the CLSID of the source filter. The <b>BSTR</b> must use the following format: <code>{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</code>.


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
 

 


---
UID: NF:segment.IMSVidFilePlayback2.put__SourceFilter
title: IMSVidFilePlayback2::put__SourceFilter (segment.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
old-location: mstv\imsvidfileplayback2_put__sourcefilter.htm
tech.root: mstv
ms.assetid: ef536087-dd2b-417f-b139-916d930e3d25
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidFilePlayback2 interface [Microsoft TV Technologies],put__SourceFilter method, IMSVidFilePlayback2.put__SourceFilter, IMSVidFilePlayback2::put__SourceFilter, IMSVidFilePlayback2put__SourceFilter, mstv.imsvidfileplayback2_put__sourcefilter, put__SourceFilter, put__SourceFilter method [Microsoft TV Technologies], put__SourceFilter method [Microsoft TV Technologies],IMSVidFilePlayback2 interface, segment/IMSVidFilePlayback2::put__SourceFilter
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
 - IMSVidFilePlayback2.put__SourceFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If the CLSID is GUID_NULL, the <a href="https://msdn.microsoft.com/da8a1d86-b3a5-4488-8bbc-82dd09aeeaca">MSVidFilePlaybackDevice</a> object uses the default source filter for the file name given in <a href="https://msdn.microsoft.com/en-us/library/Dd694558(v=VS.85).aspx">IMSVidFilePlayback::put_FileName</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694552(v=VS.85).aspx">IMSVidFilePlayback2 Interface</a>
 

 


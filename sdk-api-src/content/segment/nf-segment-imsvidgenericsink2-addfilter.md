---
UID: NF:segment.IMSVidGenericSink2.AddFilter
title: IMSVidGenericSink2::AddFilter
author: windows-driver-content
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later. .
old-location: mstv\imsvidgenericsink2_addfilter.htm
old-project: mstv
ms.assetid: b0044995-5bca-4f49-a22b-00df8f73b47f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: AddFilter, AddFilter method [Microsoft TV Technologies], AddFilter method [Microsoft TV Technologies],IMSVidGenericSink2 interface, IMSVidGenericSink2 interface [Microsoft TV Technologies],AddFilter method, IMSVidGenericSink2.AddFilter, IMSVidGenericSink2::AddFilter, IMSVidGenericSink2AddFilter, mstv.imsvidgenericsink2_addfilter, segment/IMSVidGenericSink2::AddFilter
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidGenericSink2.AddFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidGenericSink2::AddFilter


## -description




<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.</div>
<div> </div>




The <b>AddFilter</b> method specifies a DirectShow filter that is added to the graph when this segment is built.


## -parameters




### -param bstrName






#### - bstrCLSID

<b>BSTR</b> that contains the CLSID of the filter. The <b>BSTR</b> must use the following format: <code>{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</code>


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



Use this method to insert additional filters to the graph other than the sink filter. To specify the sink filter, call <a href="https://msdn.microsoft.com/51a26dc5-a551-4f97-9dd4-6522a14989a8">IMSVidGenericSink::SetSinkFilter</a>.




## -see-also




<a href="https://msdn.microsoft.com/01acd28b-a17a-413a-ab43-9656e3ab7f60">IMSVidGenericSink2 Interface</a>
 

 


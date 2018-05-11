---
UID: NF:segment.IMSVidPlayback.get_EnableResetOnStop
title: IMSVidPlayback::get_EnableResetOnStop
author: windows-driver-content
description: The get_EnableResetOnStop method indicates how playback will resume if the graph is rebuilt.
old-location: mstv\imsvidplayback_get_enableresetonstop.htm
old-project: mstv
ms.assetid: 0ea9ad29-9903-41ac-9be8-acb41cec10d1
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],get_EnableResetOnStop method, IMSVidPlayback.get_EnableResetOnStop, IMSVidPlayback::get_EnableResetOnStop, IMSVidPlaybackget_EnableResetOnStop, get_EnableResetOnStop, get_EnableResetOnStop method [Microsoft TV Technologies], get_EnableResetOnStop method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_get_enableresetonstop, segment/IMSVidPlayback::get_EnableResetOnStop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
-	IMSVidPlayback.get_EnableResetOnStop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidPlayback::get_EnableResetOnStop


## -description


The <b>get_EnableResetOnStop</b> method indicates how playback will resume if the graph is rebuilt.


## -parameters




### -param pVal [out]

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The Video Control will not seek to start of the media.</td>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The Video Control will seek to start of the media.</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
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



For more information, see <a href="https://msdn.microsoft.com/f2b4285c-3cf8-40dc-87eb-57419ef7343e">IMSVidPlayback::put_EnableResetOnStop</a>.




## -see-also




<a href="https://msdn.microsoft.com/ed954545-f58f-4841-9ffd-185350f76388">IMSVidPlayback Interface</a>
 

 


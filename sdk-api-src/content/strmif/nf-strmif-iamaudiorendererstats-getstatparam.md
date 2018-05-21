---
UID: NF:strmif.IAMAudioRendererStats.GetStatParam
title: IAMAudioRendererStats::GetStatParam
author: windows-driver-content
description: The GetStatParam method retrieves performance information from the audio renderer.
old-location: dshow\iamaudiorendererstats_getstatparam.htm
old-project: DirectShow
ms.assetid: bc01cac7-316f-4d18-ae68-c3db4dbf03fa
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetStatParam, GetStatParam method [DirectShow], GetStatParam method [DirectShow],IAMAudioRendererStats interface, IAMAudioRendererStats interface [DirectShow],GetStatParam method, IAMAudioRendererStats.GetStatParam, IAMAudioRendererStats::GetStatParam, IAMAudioRendererStatsGetStatParam, dshow.iamaudiorendererstats_getstatparam, strmif/IAMAudioRendererStats::GetStatParam
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMAudioRendererStats.GetStatParam
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAudioRendererStats::GetStatParam


## -description



The <code>GetStatParam</code> method retrieves performance information from the audio renderer.




## -parameters




### -param dwParam [in]

Specifies a member of the <a href="https://msdn.microsoft.com/ae090ab0-22e2-4407-8c16-feaa4fa20774">_AM_AUDIO_RENDERER_STAT_PARAM</a> enumeration, indicating which information to retrieve.


### -param pdwParam1 [out]

Pointer to a variable that receives performance information. The meaning of the returned value depends on the value of <i>dwParam</i>.


### -param pdwParam2 [out]

Pointer to a variable that receives performance information. The meaning of the returned value depends on the value of <i>dwParam</i>.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The renderer does not track the specified information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f5cca658-73ce-4f4d-8992-afb7824f4117">IAMAudioRendererStats Interface</a>
 

 


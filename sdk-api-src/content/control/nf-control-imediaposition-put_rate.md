---
UID: NF:control.IMediaPosition.put_Rate
title: IMediaPosition::put_Rate method
author: windows-driver-content
description: The put_Rate method sets the playback rate.
old-location: dshow\imediaposition_put_rate.htm
old-project: DirectShow
ms.assetid: fba6bb5a-6709-41e6-bf76-182c88ee42e3
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IMediaPosition, IMediaPosition interface [DirectShow], put_Rate method, IMediaPosition::put_Rate, IMediaPositionput_Rate, control/IMediaPosition::put_Rate, dshow.imediaposition_put_rate, put_Rate method [DirectShow], put_Rate method [DirectShow], IMediaPosition interface, put_Rate,IMediaPosition.put_Rate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WMPContextMenuInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMediaPosition.put_Rate
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IMediaPosition::put_Rate method


## -description



The put_Rate method sets the playback rate.




## -parameters




### -param dRate [in]

Playback rate. Must not be zero.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

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
Not implemented.

</td>
</tr>
</table>
 




## -remarks



The playback rate is expressed as a ratio of the normal speed. Thus, 1.0 is normal playback speed, 0.5 is half speed, and 2.0 is twice speed. For audio streams, changing the rate also changes the pitch.

For more information, see the remarks in <a href="https://msdn.microsoft.com/8cd44480-cadb-4b59-9fe7-4a82b3aed15b">IMediaSeeking::SetRate</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/325dd9a4-80ca-43e3-9ff8-473df1b833e9">IMediaPosition Interface</a>
 

 


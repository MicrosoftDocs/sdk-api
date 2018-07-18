---
UID: NF:control.IMediaPosition.get_Duration
title: IMediaPosition::get_Duration
author: windows-sdk-content
description: The get_Duration method retrieves the duration of the stream.
old-location: dshow\imediaposition_get_duration.htm
old-project: DirectShow
ms.assetid: 9971ca0e-a16d-4227-9efa-c965d501e6ef
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IMediaPosition interface [DirectShow],get_Duration method, IMediaPosition.get_Duration, IMediaPosition::get_Duration, IMediaPositionget_Duration, control/IMediaPosition::get_Duration, dshow.imediaposition_get_duration, get_Duration, get_Duration method [DirectShow], get_Duration method [DirectShow],IMediaPosition interface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPContextMenuInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaPosition.get_Duration
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IMediaPosition::get_Duration


## -description



The <code>get_Duration</code> method retrieves the duration of the stream.




## -parameters




### -param plength [out]

Pointer to a variable that receives the total stream length, in seconds.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

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
</table>
 




## -remarks



This method retrieves the duration of the stream at normal playback speed. Changing the playback rate does not affect the duration.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/325dd9a4-80ca-43e3-9ff8-473df1b833e9">IMediaPosition Interface</a>
 

 


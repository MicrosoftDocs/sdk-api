---
UID: NF:control.IMediaPosition.get_CurrentPosition
title: IMediaPosition::get_CurrentPosition (control.h)
description: The get_CurrentPosition method retrieves the current position, relative to the total duration of the stream.
helpviewer_keywords: ["IMediaPosition interface [DirectShow]","get_CurrentPosition method","IMediaPosition.get_CurrentPosition","IMediaPosition::get_CurrentPosition","IMediaPositionget_CurrentPosition","control/IMediaPosition::get_CurrentPosition","dshow.imediaposition_get_currentposition","get_CurrentPosition","get_CurrentPosition method [DirectShow]","get_CurrentPosition method [DirectShow]","IMediaPosition interface"]
old-location: dshow\imediaposition_get_currentposition.htm
tech.root: dshow
ms.assetid: 96f4d621-c618-49fa-a0f6-bcc68a41467e
ms.date: 12/05/2018
ms.keywords: IMediaPosition interface [DirectShow],get_CurrentPosition method, IMediaPosition.get_CurrentPosition, IMediaPosition::get_CurrentPosition, IMediaPositionget_CurrentPosition, control/IMediaPosition::get_CurrentPosition, dshow.imediaposition_get_currentposition, get_CurrentPosition, get_CurrentPosition method [DirectShow], get_CurrentPosition method [DirectShow],IMediaPosition interface
f1_keywords:
- control/IMediaPosition.get_CurrentPosition
dev_langs:
- c++
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IMediaPosition.get_CurrentPosition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaPosition::get_CurrentPosition


## -description



The <code>get_CurrentPosition</code> method retrieves the current position, relative to the total duration of the stream.




## -parameters




### -param pllTime [out]

Pointer to a variable that receives the current position, in seconds.


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



This method returns the current position that playback has reached. The value includes adjustments for the playback rate and starting time. For example, if the start time is 5 seconds, the playback rate is 2.0, and you run the graph for four seconds, the current position is 5 + (4 x 2.0) = 13.0 seconds.

If the graph is paused or stopped, the current position is the point at which playback will resume.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediaposition">IMediaPosition Interface</a>
 

 


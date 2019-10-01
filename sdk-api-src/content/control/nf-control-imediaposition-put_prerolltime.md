---
UID: NF:control.IMediaPosition.put_PrerollTime
title: IMediaPosition::put_PrerollTime (control.h)
author: windows-sdk-content
description: The put_PrerollTime method sets the amount of data that will be queued before the start position.
old-location: dshow\imediaposition_put_prerolltime.htm
tech.root: DirectShow
ms.assetid: a09e6e9f-7e6f-4e53-b805-ee4b9d97f4e7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMediaPosition interface [DirectShow],put_PrerollTime method, IMediaPosition.put_PrerollTime, IMediaPosition::put_PrerollTime, IMediaPositionput_PrerollTime, control/IMediaPosition::put_PrerollTime, dshow.imediaposition_put_prerolltime, put_PrerollTime, put_PrerollTime method [DirectShow], put_PrerollTime method [DirectShow],IMediaPosition interface
ms.topic: method
f1_keywords: 
 - "control/IMediaPosition.put_PrerollTime"
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
 - IMediaPosition.put_PrerollTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaPosition::put_PrerollTime


## -description


The <b>put_PrerollTime</b> method sets the amount of data that will be queued before the start position.


## -parameters




### -param llTime [in]

Preroll time, in seconds.


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
</table>
 




## -remarks



The <i>preroll</i> is the time prior to the start position at which nonrandom access devices, such as tape players, should start rolling.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediaposition">IMediaPosition Interface</a>
 

 


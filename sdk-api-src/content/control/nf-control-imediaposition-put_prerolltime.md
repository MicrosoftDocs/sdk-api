---
UID: NF:control.IMediaPosition.put_PrerollTime
title: IMediaPosition::put_PrerollTime
author: windows-sdk-content
description: The put_PrerollTime method sets the amount of data that will be queued before the start position.
old-location: dshow\imediaposition_put_prerolltime.htm
tech.root: DirectShow
ms.assetid: a09e6e9f-7e6f-4e53-b805-ee4b9d97f4e7
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMediaPosition interface [DirectShow],put_PrerollTime method, IMediaPosition.put_PrerollTime, IMediaPosition::put_PrerollTime, IMediaPositionput_PrerollTime, control/IMediaPosition::put_PrerollTime, dshow.imediaposition_put_prerolltime, put_PrerollTime, put_PrerollTime method [DirectShow], put_PrerollTime method [DirectShow],IMediaPosition interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- control.h
: 
- IMediaPosition.put_PrerollTime
: 
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/325dd9a4-80ca-43e3-9ff8-473df1b833e9">IMediaPosition Interface</a>
 

 


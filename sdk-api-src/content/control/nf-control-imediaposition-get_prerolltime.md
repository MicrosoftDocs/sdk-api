---
UID: NF:control.IMediaPosition.get_PrerollTime
title: IMediaPosition::get_PrerollTime
author: windows-sdk-content
description: The get_PrerollTime method retrieves the amount of data that will be queued before the start position.
old-location: dshow\imediaposition_get_prerolltime.htm
tech.root: DirectShow
ms.assetid: 3cfe9ba0-0138-4847-81ab-ea1e96e2c3a8
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IMediaPosition interface [DirectShow],get_PrerollTime method, IMediaPosition.get_PrerollTime, IMediaPosition::get_PrerollTime, IMediaPositionget_PrerollTime, control/IMediaPosition::get_PrerollTime, dshow.imediaposition_get_prerolltime, get_PrerollTime, get_PrerollTime method [DirectShow], get_PrerollTime method [DirectShow],IMediaPosition interface
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
 - IMediaPosition.get_PrerollTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaPosition::get_PrerollTime


## -description



The <code>get_PrerollTime</code> method retrieves the amount of data that will be queued before the start position.




## -parameters




### -param pllTime [out]

Pointer to a variable that receives the preroll time, in seconds.


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



The <i>preroll</i> is the time prior to the start position at which nonrandom access devices, such as tape players, should start rolling.

If no filter in the graph implements this method, the Filter Graph Manager sets the value of <i>*pllTime</i> to zero and returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/325dd9a4-80ca-43e3-9ff8-473df1b833e9">IMediaPosition Interface</a>
 

 


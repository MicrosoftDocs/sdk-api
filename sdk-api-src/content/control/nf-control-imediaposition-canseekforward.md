---
UID: NF:control.IMediaPosition.CanSeekForward
title: IMediaPosition::CanSeekForward (control.h)
author: windows-sdk-content
description: The CanSeekForward method determines whether the filter graph can seek forward in the stream.
old-location: dshow\imediaposition_canseekforward.htm
tech.root: DirectShow
ms.assetid: 0647d629-79f0-4c62-a346-8d99646469c6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CanSeekForward, CanSeekForward method [DirectShow], CanSeekForward method [DirectShow],IMediaPosition interface, IMediaPosition interface [DirectShow],CanSeekForward method, IMediaPosition.CanSeekForward, IMediaPosition::CanSeekForward, IMediaPositionCanSeekForward, control/IMediaPosition::CanSeekForward, dshow.imediaposition_canseekforward
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
 - IMediaPosition.CanSeekForward
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaPosition::CanSeekForward


## -description



The <code>CanSeekForward</code> method determines whether the filter graph can seek forward in the stream.




## -parameters




### -param pCanSeekForward [out]

Pointer to a variable that receives the value OATRUE if the graph can seek forward, or OAFALSE otherwise.


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
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd406977(v=VS.85).aspx">IMediaPosition Interface</a>
 

 


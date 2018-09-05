---
UID: NF:control.IMediaPosition.CanSeekForward
title: IMediaPosition::CanSeekForward
author: windows-sdk-content
description: The CanSeekForward method determines whether the filter graph can seek forward in the stream.
old-location: dshow\imediaposition_canseekforward.htm
old-project: DirectShow
ms.assetid: 0647d629-79f0-4c62-a346-8d99646469c6
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CanSeekForward, CanSeekForward method [DirectShow], CanSeekForward method [DirectShow],IMediaPosition interface, IMediaPosition interface [DirectShow],CanSeekForward method, IMediaPosition.CanSeekForward, IMediaPosition::CanSeekForward, IMediaPositionCanSeekForward, control/IMediaPosition::CanSeekForward, dshow.imediaposition_canseekforward
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
req.redist: 
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
 - IMediaPosition.CanSeekForward
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
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



<a href="https://msdn.microsoft.com/325dd9a4-80ca-43e3-9ff8-473df1b833e9">IMediaPosition Interface</a>
 

 


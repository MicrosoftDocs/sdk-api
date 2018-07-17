---
UID: NF:strmif.IMemInputPin.ReceiveCanBlock
title: IMemInputPin::ReceiveCanBlock
author: windows-sdk-content
description: The ReceiveCanBlock method determines whether calls to the IMemInputPin::Receive method might block.
old-location: dshow\imeminputpin_receivecanblock.htm
old-project: DirectShow
ms.assetid: cc047cad-e250-41f7-856d-26fc077f87a1
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IMemInputPin interface [DirectShow],ReceiveCanBlock method, IMemInputPin.ReceiveCanBlock, IMemInputPin::ReceiveCanBlock, IMemInputPinReceiveCanBlock, ReceiveCanBlock, ReceiveCanBlock method [DirectShow], ReceiveCanBlock method [DirectShow],IMemInputPin interface, dshow.imeminputpin_receivecanblock, strmif/IMemInputPin::ReceiveCanBlock
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMemInputPin.ReceiveCanBlock
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMemInputPin::ReceiveCanBlock


## -description



The <code>ReceiveCanBlock</code> method determines whether calls to the <a href="https://msdn.microsoft.com/7cc1e57a-a18a-4ea4-9669-0be3fb140d40">IMemInputPin::Receive</a> method might block.




## -parameters






## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The pin will not block on a call to <b>Receive</b>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The pin might block on a call to <b>Receive</b>.

</td>
</tr>
</table>
 




## -remarks



If this method returns S_FALSE, calls to the <b>Receive</b> method are guaranteed not to block. Otherwise, they might block. An upstream filter can use this method to determine its threading strategy. If calls to <b>Receive</b> can block, the upstream filter might decide to use a worker thread that buffers data.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a4407c6f-6bb5-4274-920b-8bf7d76268bc">IMemInputPin Interface</a>
 

 


---
UID: NF:strmif.IPin.ConnectedTo
title: IPin::ConnectedTo
author: windows-sdk-content
description: The ConnectedTo method retrieves a pointer to the connected pin, if any.
old-location: dshow\ipin_connectedto.htm
tech.root: DirectShow
ms.assetid: 970c814f-2309-481e-9e8e-9bd32b83fdc7
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ConnectedTo, ConnectedTo method [DirectShow], ConnectedTo method [DirectShow],IPin interface, IPin interface [DirectShow],ConnectedTo method, IPin.ConnectedTo, IPin::ConnectedTo, IPinConnectedTo, dshow.ipin_connectedto, strmif/IPin::ConnectedTo
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPin.ConnectedTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPin::ConnectedTo


## -description



The <b>ConnectedTo</b> method retrieves a pointer to the connected pin, if any.




## -parameters




### -param pPin

TBD




#### - ppPin [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface of the other pin. The caller must release the interface. This parameter cannot be <b>NULL</b>.
          


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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Pin is not connected.

</td>
</tr>
</table>
 




## -remarks



If the method succeeds, the <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface that it returns has an outstanding reference count. Be sure to release it when you are done.




## -see-also




<a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d0a906a8-bae4-43b3-8b02-ee5b97c9323d">Find an Unconnected Pin on a Filter</a>



<a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin Interface</a>
 

 


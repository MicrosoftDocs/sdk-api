---
UID: NF:strmif.IPin.ReceiveConnection
title: IPin::ReceiveConnection
author: windows-sdk-content
description: The ReceiveConnection method accepts a connection from another pin.
old-location: dshow\ipin_receiveconnection.htm
tech.root: DirectShow
ms.assetid: b2013e95-88bc-4f4a-87af-2b13c120ec46
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IPin interface [DirectShow],ReceiveConnection method, IPin.ReceiveConnection, IPin::ReceiveConnection, IPinReceiveConnection, ReceiveConnection, ReceiveConnection method [DirectShow], ReceiveConnection method [DirectShow],IPin interface, dshow.ipin_receiveconnection, strmif/IPin::ReceiveConnection
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
 - IPin.ReceiveConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPin::ReceiveConnection


## -description



The <code>ReceiveConnection</code> method accepts a connection from another pin.



Applications should not call this method. This method is called by other filters during the pin connection process.


## -parameters




### -param pConnector [in]

Pointer to the connecting pin's <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface.


### -param pmt [in]

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that specifies the media type for the connection.


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
<dt><b>VFW_E_ALREADY_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is already connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
Cannot connect while filter is active.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_TYPE_NOT_ACCEPTED</b></dt>
</dl>
</td>
<td width="60%">
The specified media type is not acceptable.

</td>
</tr>
</table>
 




## -remarks



When an output pin connects, it calls this method on the input pin. The input pin should verify that the specified media type is acceptable. It may also need to check for other connection requirements specific to the owning filter. If the connection is suitable, the input pin should return S_OK, and also do the following:

<ul>
<li>Store the media type, and return the same type in the <a href="https://msdn.microsoft.com/f372bfa7-b0ba-43f9-ba86-cbca5d1de515">IPin::ConnectionMediaType</a> method.</li>
<li>Store the output pin's <b>IPin</b> interface (<i>pConnector</i>), and return this pointer in the <a href="https://msdn.microsoft.com/970c814f-2309-481e-9e8e-9bd32b83fdc7">IPin::ConnectedTo</a> method.</li>
</ul>
If the connection is unsuitable, the pin should return an error code.

The <a href="https://msdn.microsoft.com/23b9a0e2-24fe-4ff9-b2bb-97630c237de9">CBasePin</a> class implements the basic framework for this method, including storing the media type and <b>IPin</b> pointers.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a126dd5-00fa-4ea6-b00a-09b7e1246874">How Filters Connect</a>



<a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin Interface</a>
 

 


---
UID: NF:strmif.IPin.Connect
title: IPin::Connect
author: windows-driver-content
description: The Connect method connects the pin to another pin.
old-location: dshow\ipin_connect.htm
old-project: DirectShow
ms.assetid: 1b02ee67-5dc5-44c1-bea5-2eab46ebd0f6
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: Connect, Connect method [DirectShow], Connect method [DirectShow],IPin interface, IPin interface [DirectShow],Connect method, IPin.Connect, IPin::Connect, IPinConnect, dshow.ipin_connect, strmif/IPin::Connect
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IPin.Connect
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IPin::Connect


## -description



The <code>Connect</code> method connects the pin to another pin.



Applications should not call this method. Use <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> methods instead. This method is called by the Filter Graph Manager to connect pins.


## -parameters




### -param pReceivePin [in]

Pointer to the receiving pin's <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface.


### -param pmt [in]

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that specifies the media type for the connection. Can be <b>NULL</b>.


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
<dt><b>VFW_E_NO_ACCEPTABLE_TYPES</b></dt>
</dl>
</td>
<td width="60%">
Cannot find an acceptable media type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NO_TRANSPORT</b></dt>
</dl>
</td>
<td width="60%">
Pins cannot agree on a transport, or there is no allocator for the connection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter is active and the pin does not support dynamic reconnection.

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



The <i>pmt</i> parameter can be <b>NULL</b>. It can also specify a partial media type, with a value of GUID_NULL for the major type, subtype, or format.

This method verifies that the connection is possible. If the pin rejects the connection, the method fails. The connecting pin proposes media types by calling <a href="https://msdn.microsoft.com/b2013e95-88bc-4f4a-87af-2b13c120ec46">IPin::ReceiveConnection</a> on the receiving pin.




## -see-also




<a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin Interface</a>
 

 


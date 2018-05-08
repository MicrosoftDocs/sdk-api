---
UID: NF:strmif.IPin.Disconnect
title: IPin::Disconnect
author: windows-driver-content
description: The Disconnect method breaks the current pin connection.
old-location: dshow\ipin_disconnect.htm
old-project: DirectShow
ms.assetid: 46e1e99c-848b-4936-b6bf-4ef1703a1f42
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: Disconnect, Disconnect method [DirectShow], Disconnect method [DirectShow],IPin interface, IPin interface [DirectShow],Disconnect method, IPin.Disconnect, IPin::Disconnect, IPinDisconnect, dshow.ipin_disconnect, strmif/IPin::Disconnect
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
-	IPin.Disconnect
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IPin::Disconnect


## -description



The <code>Disconnect</code> method breaks the current pin connection.



The Filter Graph Manager calls this method when it disconnects two filters. Applications and filters should not call this method. Instead, call the <a href="https://msdn.microsoft.com/8c7d6cb6-b91c-4461-8f2b-38342a88eafc">IFilterGraph::Disconnect</a> method on the Filter Graph Manager.


## -parameters






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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The pin was not connected.

</td>
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
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter is active.

</td>
</tr>
</table>
 




## -remarks



This method fails if the filter is paused or running. If the pin supports the <a href="https://msdn.microsoft.com/0843a01c-6f6a-4765-abca-dd562175fcee">IPinConnection</a> interface, call <a href="https://msdn.microsoft.com/44a5a219-fd42-4fe1-a767-f74d01d86012">IPinConnection::DynamicDisconnect</a> to disconnect the pin when the filter is paused or running.

This method does not disconnect the other pin in the pin connection.




## -see-also




<a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin Interface</a>
 

 


---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITfMouseTrackerACP::AdviseMouseSink


## -description




## -parameters




### -param range [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> interface that specifies the range of text that the mouse sink is installed for.


### -param pSink [in]

Pointer to the <a href="https://msdn.microsoft.com/d6e5549e-768d-47af-a553-84430641cda4">ITfMouseSink</a> interface. The application must increment this object reference count and save the interface.


### -param pdwCookie [out]

Pointer to a DWORD that receives a cookie that identifies the mouse event sink.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The application does not support mouse event sinks.

</td>
</tr>
</table>
 




## -remarks



When this advise sink is installed, a mouse event that occurs over the range specified by <i>range</i> will result in the mouse event sink <a href="https://msdn.microsoft.com/1aa4fdb7-b16d-4e58-934a-8323450f6749">ITfMouseSink::OnMouseEvent</a> method being called.

The value placed in <i>pdwCookie</i> will be saved by the caller and passed to the <a href="https://msdn.microsoft.com/6c753e09-f67a-45d6-b2f9-c08d5c05c04d">ITfMouseTrackerACP::UnadviseMouseSink</a> method to remove the mouse event sink.




## -see-also




<a href="https://msdn.microsoft.com/d6e5549e-768d-47af-a553-84430641cda4">
        ITfMouseSink
      </a>



<a href="https://msdn.microsoft.com/1aa4fdb7-b16d-4e58-934a-8323450f6749">
        ITfMouseSink::OnMouseEvent
      </a>



<a href="https://msdn.microsoft.com/6761cf80-60b1-4c3a-8c3f-f040fab60f24">ITfMouseTrackerACP</a>



<a href="https://msdn.microsoft.com/6c753e09-f67a-45d6-b2f9-c08d5c05c04d">
        ITfMouseTrackerACP::UnadviseMouseSink
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 


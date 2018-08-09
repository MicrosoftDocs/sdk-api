---
UID: NF:segment.IMSVidVideoRendererDevices.get__NewEnum
title: IMSVidVideoRendererDevices::get__NewEnum
author: windows-sdk-content
description: The get__NewEnum method retrieves an enumerator for the collection.
old-location: mstv\imsvidvideorendererdevices_get__newenum.htm
old-project: mstv
ms.assetid: da321f4c-801a-4e27-bc82-5dab723adf97
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidVideoRendererDevices interface [Microsoft TV Technologies],get__NewEnum method, IMSVidVideoRendererDevices.get__NewEnum, IMSVidVideoRendererDevices::get__NewEnum, IMSVidVideoRendererDevicesget__NewEnum, get__NewEnum, get__NewEnum method [Microsoft TV Technologies], get__NewEnum method [Microsoft TV Technologies],IMSVidVideoRendererDevices interface, mstv.imsvidvideorendererdevices_get__newenum, segment/IMSVidVideoRendererDevices::get__NewEnum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidVideoRendererDevices.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidVideoRendererDevices::get__NewEnum


## -description


The <b>get__NewEnum</b> method retrieves an enumerator for the collection.


## -parameters




### -param pD






#### - ppD [out]

Pointer to a variable that receives an <b>IEnumVARIANT</b> interface pointer.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
</table>
 




## -remarks



This method is provided so that Automation clients can iterate through the collection using a <code>For...Each</code> loop.

The returned <b>IEnumVARIANT</b> interface is not thread safe, because it is intended primarily for use by Automation clients. Clients should not call methods on the interface from more than one thread. (C++ applications should generally use the <a href="https://msdn.microsoft.com/2cb169d2-f6b2-4156-aa11-f9b47437b731">IMSVidVideoRendererDevices::get_Item</a> method instead.)

If the method succeeds, the <b>IEnumVARIANT</b> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/cf8e1307-b4a5-464b-b9a6-32c195941309">IMSVidVideoRendererDevices Interface</a>
 

 


---
UID: NF:wmp.IWMPCore.get_mediaCollection
title: IWMPCore::get_mediaCollection
author: windows-sdk-content
description: The get_mediaCollection method retrieves a pointer to an IWMPMediaCollection interface.
old-location: wmp\iwmpcore_get_mediacollection.htm
tech.root: WMP
ms.assetid: 41b090ca-edf0-440e-b578-26c5ad064657
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_mediaCollection method, IWMPCore.get_mediaCollection, IWMPCore::get_mediaCollection, IWMPCoreget_mediaCollection, get_mediaCollection, get_mediaCollection method [Windows Media Player], get_mediaCollection method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_mediacollection, wmp/IWMPCore::get_mediaCollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPCore.get_mediaCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPCore::get_mediaCollection


## -description



The <b>get_mediaCollection</b> method retrieves a pointer to an <b>IWMPMediaCollection</b> interface.




## -parameters




### -param ppMediaCollection [out]

Pointer to a pointer to an <b>IWMPMediaCollection</b> interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>



<a href="https://msdn.microsoft.com/bf975a30-dfb1-4994-9095-510a6b997aff">IWMPMediaCollection Interface</a>
 

 


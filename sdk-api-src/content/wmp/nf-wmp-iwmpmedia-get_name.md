---
UID: NF:wmp.IWMPMedia.get_name
title: IWMPMedia::get_name
author: windows-sdk-content
description: The get_name method retrieves the name of the media item.
old-location: wmp\iwmpmedia_get_name.htm
tech.root: WMP
ms.assetid: 83bb3495-a12d-48a8-864c-3cd636866308
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWMPMedia interface [Windows Media Player],get_name method, IWMPMedia.get_name, IWMPMedia2 interface [Windows Media Player],get_name method, IWMPMedia2::get_name, IWMPMedia3 interface [Windows Media Player],get_name method, IWMPMedia3::get_name, IWMPMedia::get_name, IWMPMediaget_name, get_name, get_name method [Windows Media Player], get_name method [Windows Media Player],IWMPMedia interface, get_name method [Windows Media Player],IWMPMedia2 interface, get_name method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_get_name, wmp/IWMPMedia2::get_name, wmp/IWMPMedia3::get_name, wmp/IWMPMedia::get_name
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
 - IWMPMedia.get_name
 - IWMPMedia2.get_name
 - IWMPMedia3.get_name
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPMedia::get_name


## -description



The <b>get_name</b> method retrieves the name of the media item.




## -parameters




### -param pbstrName [out]

Pointer to a <b>BSTR</b> containing the name.


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




<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/2cf6cff8-c5d1-4d10-8d32-764e35ef7ba2">IWMPMedia::put_name</a>
 

 


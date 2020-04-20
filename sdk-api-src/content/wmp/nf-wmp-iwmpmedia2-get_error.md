---
UID: NF:wmp.IWMPMedia2.get_error
title: IWMPMedia2::get_error (wmp.h)
description: The get_error method retrieves a pointer to an IWMPErrorItem interface if the media item has an error condition.helpviewer_keywords: ["IWMPMedia2 interface [Windows Media Player]","get_error method","IWMPMedia2.get_error","IWMPMedia2::get_error","IWMPMedia2get_error","IWMPMedia3 interface [Windows Media Player]","get_error method","IWMPMedia3::get_error","get_error","get_error method [Windows Media Player]","get_error method [Windows Media Player]","IWMPMedia2 interface","get_error method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia2_get_error","wmp/IWMPMedia2::get_error","wmp/IWMPMedia3::get_error"]
old-location: wmp\iwmpmedia2_get_error.htm
tech.root: WMP
ms.assetid: 55df580e-1a51-450e-80d9-53398f3b4d9d
ms.date: 12/05/2018
ms.keywords: IWMPMedia2 interface [Windows Media Player],get_error method, IWMPMedia2.get_error, IWMPMedia2::get_error, IWMPMedia2get_error, IWMPMedia3 interface [Windows Media Player],get_error method, IWMPMedia3::get_error, get_error, get_error method [Windows Media Player], get_error method [Windows Media Player],IWMPMedia2 interface, get_error method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia2_get_error, wmp/IWMPMedia2::get_error, wmp/IWMPMedia3::get_error
f1_keywords:
- wmp/IWMPMedia2.get_error
dev_langs:
- c++
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
- IWMPMedia2.get_error
- IWMPMedia3.get_error
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPMedia2::get_error


## -description



The <b>get_error</b> method retrieves a pointer to an <b>IWMPErrorItem</b> interface if the media item has an error condition.




## -parameters




### -param ppIWMPErrorItem [out]

Pointer to a pointer to an <b>IWMPErrorItem</b> interface.


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



If the media item cannot be played, this property retrieves an <b>IWMPErrorItem</b> interface that contains information about the problem encountered.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmperroritem">IWMPErrorItem Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmedia2">IWMPMedia2 Interface</a>
 

 


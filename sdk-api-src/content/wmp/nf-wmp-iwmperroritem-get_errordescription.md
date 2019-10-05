---
UID: NF:wmp.IWMPErrorItem.get_errorDescription
title: IWMPErrorItem::get_errorDescription (wmp.h)
author: windows-sdk-content
description: The get_errorDescription method retrieves a description of the error.
old-location: wmp\iwmperroritem_get_errordescription.htm
tech.root: WMP
ms.assetid: eb322580-2cc6-4094-9da3-9b8d78a5cb48
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPErrorItem interface [Windows Media Player],get_errorDescription method, IWMPErrorItem.get_errorDescription, IWMPErrorItem::get_errorDescription, IWMPErrorItemget_errorDescription, get_errorDescription, get_errorDescription method [Windows Media Player], get_errorDescription method [Windows Media Player],IWMPErrorItem interface, wmp.iwmperroritem_get_errordescription, wmp/IWMPErrorItem::get_errorDescription
ms.topic: method
f1_keywords: 
 - "wmp/IWMPErrorItem.get_errorDescription"
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
 - IWMPErrorItem.get_errorDescription
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPErrorItem::get_errorDescription


## -description



The <b>get_errorDescription</b> method retrieves a description of the error.




## -parameters




### -param pbstrDescription [out]

Pointer to a <b>BSTR</b> containing the description.


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



You should set a <b>VARIANT_BOOL</b> to <b>FALSE</b> and pass it into <b>IWMPSettings::put_enableErrorDialogs</b> if you choose to display custom error messages.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmperroritem">IWMPErrorItem Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-put_enableerrordialogs">IWMPSettings::put_enableErrorDialogs</a>
 

 


---
UID: NF:wmp.IWMPErrorItem.get_errorCode
title: IWMPErrorItem::get_errorCode (wmp.h)
description: The get_errorCode method retrieves the current error code.helpviewer_keywords: ["IWMPErrorItem interface [Windows Media Player]","get_errorCode method","IWMPErrorItem.get_errorCode","IWMPErrorItem::get_errorCode","IWMPErrorItemget_errorCode","get_errorCode","get_errorCode method [Windows Media Player]","get_errorCode method [Windows Media Player]","IWMPErrorItem interface","wmp.iwmperroritem_get_errorcode","wmp/IWMPErrorItem::get_errorCode"]
old-location: wmp\iwmperroritem_get_errorcode.htm
tech.root: WMP
ms.assetid: e809a1bf-1c7e-4006-9d27-e9921f2f14b2
ms.date: 12/05/2018
ms.keywords: IWMPErrorItem interface [Windows Media Player],get_errorCode method, IWMPErrorItem.get_errorCode, IWMPErrorItem::get_errorCode, IWMPErrorItemget_errorCode, get_errorCode, get_errorCode method [Windows Media Player], get_errorCode method [Windows Media Player],IWMPErrorItem interface, wmp.iwmperroritem_get_errorcode, wmp/IWMPErrorItem::get_errorCode
f1_keywords:
- wmp/IWMPErrorItem.get_errorCode
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
- IWMPErrorItem.get_errorCode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPErrorItem::get_errorCode


## -description



The <b>get_errorCode</b> method retrieves the current error code.




## -parameters




### -param phr [out]

Pointer to a <b>long</b> containing the error code.


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
 

 


---
UID: NF:wmp.IWMPLibrary.get_name
title: IWMPLibrary::get_name (wmp.h)
description: The get_name method retrieves the display name of the current library.
helpviewer_keywords: ["IWMPLibrary interface [Windows Media Player]","get_name method","IWMPLibrary.get_name","IWMPLibrary::get_name","IWMPLibraryget_name","get_name","get_name method [Windows Media Player]","get_name method [Windows Media Player]","IWMPLibrary interface","wmp.iwmplibrary_get_name","wmp/IWMPLibrary::get_name"]
old-location: wmp\iwmplibrary_get_name.htm
tech.root: WMP
ms.assetid: 28f1e3bc-3692-4fd0-a0b3-fecc3a173103
ms.date: 12/05/2018
ms.keywords: IWMPLibrary interface [Windows Media Player],get_name method, IWMPLibrary.get_name, IWMPLibrary::get_name, IWMPLibraryget_name, get_name, get_name method [Windows Media Player], get_name method [Windows Media Player],IWMPLibrary interface, wmp.iwmplibrary_get_name, wmp/IWMPLibrary::get_name
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPLibrary::get_name
 - wmp/IWMPLibrary::get_name
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPLibrary.get_name
---

# IWMPLibrary::get_name


## -description

The <b>get_name</b> method retrieves the display name of the current library.

## -parameters

### -param pbstrName [out]

Pointer to a string containing the name of the current library.

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

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmplibrary">IWMPLibrary Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type">IWMPLibrary::get_type</a>
---
UID: NF:wmp.IWMPCore.get_mediaCollection
title: IWMPCore::get_mediaCollection (wmp.h)
description: The get_mediaCollection method retrieves a pointer to an IWMPMediaCollection interface.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","get_mediaCollection method","IWMPCore.get_mediaCollection","IWMPCore::get_mediaCollection","IWMPCoreget_mediaCollection","get_mediaCollection","get_mediaCollection method [Windows Media Player]","get_mediaCollection method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_get_mediacollection","wmp/IWMPCore::get_mediaCollection"]
old-location: wmp\iwmpcore_get_mediacollection.htm
tech.root: WMP
ms.assetid: 41b090ca-edf0-440e-b578-26c5ad064657
ms.date: 12/05/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_mediaCollection method, IWMPCore.get_mediaCollection, IWMPCore::get_mediaCollection, IWMPCoreget_mediaCollection, get_mediaCollection, get_mediaCollection method [Windows Media Player], get_mediaCollection method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_mediacollection, wmp/IWMPCore::get_mediaCollection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPCore::get_mediaCollection
 - wmp/IWMPCore::get_mediaCollection
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
 - IWMPCore.get_mediaCollection
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

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection Interface</a>
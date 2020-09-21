---
UID: NF:wmp.IWMPCdromCollection.item
title: IWMPCdromCollection::item (wmp.h)
description: The item method retrieves a pointer to an IWMPCdrom interface at the given index.
helpviewer_keywords: ["IWMPCdromCollection interface [Windows Media Player]","item method","IWMPCdromCollection.item","IWMPCdromCollection::item","IWMPCdromCollectionitem","item","item method [Windows Media Player]","item method [Windows Media Player]","IWMPCdromCollection interface","wmp.iwmpcdromcollection_item","wmp/IWMPCdromCollection::item"]
old-location: wmp\iwmpcdromcollection_item.htm
tech.root: WMP
ms.assetid: 4604e53d-914f-4888-99c7-64d0683ac2e0
ms.date: 12/05/2018
ms.keywords: IWMPCdromCollection interface [Windows Media Player],item method, IWMPCdromCollection.item, IWMPCdromCollection::item, IWMPCdromCollectionitem, item, item method [Windows Media Player], item method [Windows Media Player],IWMPCdromCollection interface, wmp.iwmpcdromcollection_item, wmp/IWMPCdromCollection::item
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
 - IWMPCdromCollection::item
 - wmp/IWMPCdromCollection::item
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
 - IWMPCdromCollection.item
---

# IWMPCdromCollection::item


## -description

The <b>item</b> method retrieves a pointer to an <b>IWMPCdrom</b> interface at the given index.

## -parameters

### -param lIndex [in]

<b>long</b> containing the index.

### -param ppItem [out]

Pointer to a pointer to an <b>IWMPCdrom</b> interface.

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

To use this method, read access to the library is required. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdrom">IWMPCdrom Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection">IWMPCdromCollection Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count">IWMPCdromCollection::get_count</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_drivespecifier">IWMPCdromCollection::get_driveSpecifier</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_name">IWMPPlaylist::get_name</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-get_mediaaccessrights">IWMPSettings2::get_mediaAccessRights</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-requestmediaaccessrights">IWMPSettings2::requestMediaAccessRights</a>
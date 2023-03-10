---
UID: NF:wmp.IWMPCdromCollection.getByDriveSpecifier
title: IWMPCdromCollection::getByDriveSpecifier (wmp.h)
description: The getByDriveSpecifier method retrieves a pointer to an IWMPCdrom interface associated with a particular drive letter.
helpviewer_keywords: ["IWMPCdromCollection interface [Windows Media Player]","getByDriveSpecifier method","IWMPCdromCollection.getByDriveSpecifier","IWMPCdromCollection::getByDriveSpecifier","IWMPCdromCollectiongetByDriveSpecifier","getByDriveSpecifier","getByDriveSpecifier method [Windows Media Player]","getByDriveSpecifier method [Windows Media Player]","IWMPCdromCollection interface","wmp.iwmpcdromcollection_getbydrivespecifier","wmp/IWMPCdromCollection::getByDriveSpecifier"]
old-location: wmp\iwmpcdromcollection_getbydrivespecifier.htm
tech.root: WMP
ms.assetid: b48679da-c8f3-4e9d-89cd-0ecbcbc07fe4
ms.date: 12/05/2018
ms.keywords: IWMPCdromCollection interface [Windows Media Player],getByDriveSpecifier method, IWMPCdromCollection.getByDriveSpecifier, IWMPCdromCollection::getByDriveSpecifier, IWMPCdromCollectiongetByDriveSpecifier, getByDriveSpecifier, getByDriveSpecifier method [Windows Media Player], getByDriveSpecifier method [Windows Media Player],IWMPCdromCollection interface, wmp.iwmpcdromcollection_getbydrivespecifier, wmp/IWMPCdromCollection::getByDriveSpecifier
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
 - IWMPCdromCollection::getByDriveSpecifier
 - wmp/IWMPCdromCollection::getByDriveSpecifier
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
 - IWMPCdromCollection.getByDriveSpecifier
---

# IWMPCdromCollection::getByDriveSpecifier


## -description

The <b>getByDriveSpecifier</b> method retrieves a pointer to an <b>IWMPCdrom</b> interface associated with a particular drive letter.

## -parameters

### -param bstrDriveSpecifier [in]

<b>BSTR</b> containing the drive letter followed by a colon (":") character.

### -param ppCdrom [out]

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

Drive letters must be given in the form <i>X</i>:, where <i>X</i> represents the drive letter.

To use this method, read access to the library is required. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdrom">IWMPCdrom Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-eject">IWMPCdrom::eject</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection">IWMPCdromCollection Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-get_mediaaccessrights">IWMPSettings2::get_mediaAccessRights</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-requestmediaaccessrights">IWMPSettings2::requestMediaAccessRights</a>
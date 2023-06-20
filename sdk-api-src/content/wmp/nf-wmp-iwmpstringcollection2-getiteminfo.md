---
UID: NF:wmp.IWMPStringCollection2.getItemInfo
title: IWMPStringCollection2::getItemInfo (wmp.h)
description: The getItemInfo method retrieves the string corresponding to the specified string collection item index and name.
helpviewer_keywords: ["IWMPStringCollection2 interface [Windows Media Player]","getItemInfo method","IWMPStringCollection2.getItemInfo","IWMPStringCollection2::getItemInfo","IWMPStringCollection2getItemInfo","getItemInfo","getItemInfo method [Windows Media Player]","getItemInfo method [Windows Media Player]","IWMPStringCollection2 interface","wmp.iwmpstringcollection2_getiteminfo","wmp/IWMPStringCollection2::getItemInfo"]
old-location: wmp\iwmpstringcollection2_getiteminfo.htm
tech.root: WMP
ms.assetid: 1915d71f-aca3-4943-a4da-ed8f2fa3f46d
ms.date: 4/26/2023
ms.keywords: IWMPStringCollection2 interface [Windows Media Player],getItemInfo method, IWMPStringCollection2.getItemInfo, IWMPStringCollection2::getItemInfo, IWMPStringCollection2getItemInfo, getItemInfo, getItemInfo method [Windows Media Player], getItemInfo method [Windows Media Player],IWMPStringCollection2 interface, wmp.iwmpstringcollection2_getiteminfo, wmp/IWMPStringCollection2::getItemInfo
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
 - IWMPStringCollection2::getItemInfo
 - wmp/IWMPStringCollection2::getItemInfo
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
 - IWMPStringCollection2.getItemInfo
---

# IWMPStringCollection2::getItemInfo


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getItemInfo</b> method retrieves the string corresponding to the specified string collection item index and name.

## -parameters

### -param lCollectionIndex [in]

A <b>long</b> specifying the zero-based index of the string collection item from which to get the attribute.

### -param bstrItemName [in]

<b>BSTR</b> containing the attribute name.

### -param pbstrValue [out]

Pointer to a <b>BSTR</b> that receives the string. For attributes whose underlying value is <b>Boolean</b>, it returns the string "true" or "false".

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

To retrieve attributes with multiple values and attributes with complex values, use the <b>getItemInfoByType</b> method.

To use this method, read access to the library is required. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2">IWMPStringCollection2 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpstringcollection2-getiteminfobytype">IWMPStringCollection2::getItemInfoByType</a>
---
UID: NF:wmp.IWMPMediaCollection.remove
title: IWMPMediaCollection::remove (wmp.h)
description: The remove method removes a specified item from the media collection.
helpviewer_keywords: ["IWMPMediaCollection interface [Windows Media Player]","remove method","IWMPMediaCollection.remove","IWMPMediaCollection::remove","IWMPMediaCollectionremove","remove","remove method [Windows Media Player]","remove method [Windows Media Player]","IWMPMediaCollection interface","wmp.iwmpmediacollection_remove","wmp/IWMPMediaCollection::remove"]
old-location: wmp\iwmpmediacollection_remove.htm
tech.root: WMP
ms.assetid: 646d2e3c-623b-4040-af82-1cefac6fc1ae
ms.date: 4/26/2023
ms.keywords: IWMPMediaCollection interface [Windows Media Player],remove method, IWMPMediaCollection.remove, IWMPMediaCollection::remove, IWMPMediaCollectionremove, remove, remove method [Windows Media Player], remove method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_remove, wmp/IWMPMediaCollection::remove
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
 - IWMPMediaCollection::remove
 - wmp/IWMPMediaCollection::remove
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
 - IWMPMediaCollection.remove
---

# IWMPMediaCollection::remove


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>remove</b> method removes a specified item from the media collection.

## -parameters

### -param pItem [in]

Pointer to an <b>IWMPMedia</b> interface that identifies the item to remove.

### -param varfDeleteFile [in]

Specifies whether the method should remove the specified item.

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

This method deletes an item from the library. This method does not delete files from the user's computer.

Before calling this method, you must have read access to the library. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-add">IWMPMediaCollection::add</a>
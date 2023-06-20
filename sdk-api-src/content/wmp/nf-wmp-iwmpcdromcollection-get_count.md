---
UID: NF:wmp.IWMPCdromCollection.get_count
title: IWMPCdromCollection::get_count (wmp.h)
description: The get_count method retrieves the number of available CD and DVD drives on the system.
helpviewer_keywords: ["IWMPCdromCollection interface [Windows Media Player]","get_count method","IWMPCdromCollection.get_count","IWMPCdromCollection::get_count","IWMPCdromCollectionget_count","get_count","get_count method [Windows Media Player]","get_count method [Windows Media Player]","IWMPCdromCollection interface","wmp.iwmpcdromcollection_get_count","wmp/IWMPCdromCollection::get_count"]
old-location: wmp\iwmpcdromcollection_get_count.htm
tech.root: WMP
ms.assetid: 0e0c73b3-463c-43de-b1b8-5644a377bfd1
ms.date: 4/26/2023
ms.keywords: IWMPCdromCollection interface [Windows Media Player],get_count method, IWMPCdromCollection.get_count, IWMPCdromCollection::get_count, IWMPCdromCollectionget_count, get_count, get_count method [Windows Media Player], get_count method [Windows Media Player],IWMPCdromCollection interface, wmp.iwmpcdromcollection_get_count, wmp/IWMPCdromCollection::get_count
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
 - IWMPCdromCollection::get_count
 - wmp/IWMPCdromCollection::get_count
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
 - IWMPCdromCollection.get_count
---

# IWMPCdromCollection::get_count


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_count</b> method retrieves the number of available CD and DVD drives on the system.

## -parameters

### -param plCount [out]

Pointer to a <b>long</b> containing the count.

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

To retrieve the value of this property, read access to the library is required. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

DVD drives are counted exactly like CD drives. However, the Windows Media Player ActiveX control only supports DVD functionality for Windows XP or later. Typically, DVD drives can play CD media, but CD drives cannot play DVD media.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>long</b> set to 0.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection">IWMPCdromCollection Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-get_mediaaccessrights">IWMPSettings2::get_mediaAccessRights</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-requestmediaaccessrights">IWMPSettings2::requestMediaAccessRights</a>
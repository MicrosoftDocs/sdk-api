---
UID: NF:wmp.IWMPQuery.beginNextGroup
title: IWMPQuery::beginNextGroup (wmp.h)
description: The beginNextGroup method begins a new condition group.
helpviewer_keywords: ["IWMPQuery interface [Windows Media Player]","beginNextGroup method","IWMPQuery.beginNextGroup","IWMPQuery::beginNextGroup","IWMPQuerybeginNextGroup","beginNextGroup","beginNextGroup method [Windows Media Player]","beginNextGroup method [Windows Media Player]","IWMPQuery interface","wmp.iwmpquery_beginnextgroup","wmp/IWMPQuery::beginNextGroup"]
old-location: wmp\iwmpquery_beginnextgroup.htm
tech.root: WMP
ms.assetid: c81a8125-2cfa-40e2-afc5-672c2866b880
ms.date: 4/26/2023
ms.keywords: IWMPQuery interface [Windows Media Player],beginNextGroup method, IWMPQuery.beginNextGroup, IWMPQuery::beginNextGroup, IWMPQuerybeginNextGroup, beginNextGroup, beginNextGroup method [Windows Media Player], beginNextGroup method [Windows Media Player],IWMPQuery interface, wmp.iwmpquery_beginnextgroup, wmp/IWMPQuery::beginNextGroup
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
 - IWMPQuery::beginNextGroup
 - wmp/IWMPQuery::beginNextGroup
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
 - IWMPQuery.beginNextGroup
---

# IWMPQuery::beginNextGroup


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>beginNextGroup</b> method begins a new condition group.



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

Beginning a new condition group implies that you have completed the current condition group. The new condition group is always concatenated to the previous condition group by using OR logic.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-createquery">IWMPMediaCollection2::createQuery</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getplaylistbyquery">IWMPMediaCollection2::getPlaylistByQuery</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getstringcollectionbyquery">IWMPMediaCollection2::getStringCollectionByQuery</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpquery">IWMPQuery Interface</a>

---
UID: NF:wmp.IWMPMediaCollection2.createQuery
title: IWMPMediaCollection2::createQuery (wmp.h)
description: The createQuery method retrieves a pointer to an IWMPQuery interface that represents a new query.
helpviewer_keywords: ["IWMPMediaCollection2 interface [Windows Media Player]","createQuery method","IWMPMediaCollection2.createQuery","IWMPMediaCollection2::createQuery","IWMPMediaCollection2createQuery","createQuery","createQuery method [Windows Media Player]","createQuery method [Windows Media Player]","IWMPMediaCollection2 interface","wmp.iwmpmediacollection2_createquery","wmp/IWMPMediaCollection2::createQuery"]
old-location: wmp\iwmpmediacollection2_createquery.htm
tech.root: WMP
ms.assetid: b1e6bf08-3b81-4c04-92ff-73eac5f7495a
ms.date: 4/26/2023
ms.keywords: IWMPMediaCollection2 interface [Windows Media Player],createQuery method, IWMPMediaCollection2.createQuery, IWMPMediaCollection2::createQuery, IWMPMediaCollection2createQuery, createQuery, createQuery method [Windows Media Player], createQuery method [Windows Media Player],IWMPMediaCollection2 interface, wmp.iwmpmediacollection2_createquery, wmp/IWMPMediaCollection2::createQuery
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
 - IWMPMediaCollection2::createQuery
 - wmp/IWMPMediaCollection2::createQuery
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
 - IWMPMediaCollection2.createQuery
---

# IWMPMediaCollection2::createQuery


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>createQuery</b> method retrieves a pointer to an <b>IWMPQuery</b> interface that represents a new query.

## -parameters

### -param ppQuery [out]

Address of a variable that receives an <b>IWMPQuery</b> pointer to the new, empty query.

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

Creating a new query is the first step toward creating a compound query.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2">IWMPMediaCollection2 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpquery">IWMPQuery Interface</a>
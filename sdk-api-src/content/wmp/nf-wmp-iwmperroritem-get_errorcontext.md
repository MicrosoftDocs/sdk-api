---
UID: NF:wmp.IWMPErrorItem.get_errorContext
title: IWMPErrorItem::get_errorContext (wmp.h)
description: The get_errorContext method retrieves a value indicating the context of the error.
helpviewer_keywords: ["IWMPErrorItem interface [Windows Media Player]","get_errorContext method","IWMPErrorItem.get_errorContext","IWMPErrorItem::get_errorContext","IWMPErrorItemget_errorContext","get_errorContext","get_errorContext method [Windows Media Player]","get_errorContext method [Windows Media Player]","IWMPErrorItem interface","wmp.iwmperroritem_get_errorcontext","wmp/IWMPErrorItem::get_errorContext"]
old-location: wmp\iwmperroritem_get_errorcontext.htm
tech.root: WMP
ms.assetid: 575f14e7-7a5b-4000-9957-253c40b1ef62
ms.date: 4/26/2023
ms.keywords: IWMPErrorItem interface [Windows Media Player],get_errorContext method, IWMPErrorItem.get_errorContext, IWMPErrorItem::get_errorContext, IWMPErrorItemget_errorContext, get_errorContext, get_errorContext method [Windows Media Player], get_errorContext method [Windows Media Player],IWMPErrorItem interface, wmp.iwmperroritem_get_errorcontext, wmp/IWMPErrorItem::get_errorContext
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
 - IWMPErrorItem::get_errorContext
 - wmp/IWMPErrorItem::get_errorContext
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
 - IWMPErrorItem.get_errorContext
---

# IWMPErrorItem::get_errorContext


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_errorContext</b> method retrieves a value indicating the context of the error.

## -parameters

### -param pvarContext [out]

Pointer to a <b>VARIANT</b> containing the error context.

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

The error context is information that is used by Microsoft to provide additional information for technical support personnel.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT</b> with the <b>vt</b> field set to VT_EMPTY.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmperroritem">IWMPErrorItem Interface</a>
---
UID: NF:wmp.IWMPError.clearErrorQueue
title: IWMPError::clearErrorQueue (wmp.h)
description: The clearErrorQueue method clears the errors from the error queue.
helpviewer_keywords: ["IWMPError interface [Windows Media Player]","clearErrorQueue method","IWMPError.clearErrorQueue","IWMPError::clearErrorQueue","IWMPErrorclearErrorQueue","clearErrorQueue","clearErrorQueue method [Windows Media Player]","clearErrorQueue method [Windows Media Player]","IWMPError interface","wmp.iwmperror_clearerrorqueue","wmp/IWMPError::clearErrorQueue"]
old-location: wmp\iwmperror_clearerrorqueue.htm
tech.root: WMP
ms.assetid: 8c965b48-d178-4b41-add7-0b7d208380a3
ms.date: 4/26/2023
ms.keywords: IWMPError interface [Windows Media Player],clearErrorQueue method, IWMPError.clearErrorQueue, IWMPError::clearErrorQueue, IWMPErrorclearErrorQueue, clearErrorQueue, clearErrorQueue method [Windows Media Player], clearErrorQueue method [Windows Media Player],IWMPError interface, wmp.iwmperror_clearerrorqueue, wmp/IWMPError::clearErrorQueue
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
 - IWMPError::clearErrorQueue
 - wmp/IWMPError::clearErrorQueue
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
 - IWMPError.clearErrorQueue
---

# IWMPError::clearErrorQueue


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>clearErrorQueue</b> method clears the errors from the error queue.



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

Use this method to clear the error queue after a series of errors has been processed.

You should set a <b>VARIANT_BOOL</b> to <b>FALSE</b> and pass it into <b>IWMPSettings::put_enableErrorDialogs</b> if you choose to display custom error messages.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmperror">IWMPError Interface</a>

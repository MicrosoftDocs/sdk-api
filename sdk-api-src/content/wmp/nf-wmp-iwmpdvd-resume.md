---
UID: NF:wmp.IWMPDVD.resume
title: IWMPDVD::resume (wmp.h)
description: The resume method returns to playback mode from menu mode at the same title position as when the menu was invoked.
helpviewer_keywords: ["IWMPDVD interface [Windows Media Player]","resume method","IWMPDVD.resume","IWMPDVD::resume","IWMPDVDresume","resume","resume method [Windows Media Player]","resume method [Windows Media Player]","IWMPDVD interface","wmp.iwmpdvd_resume","wmp/IWMPDVD::resume"]
old-location: wmp\iwmpdvd_resume.htm
tech.root: WMP
ms.assetid: c0817edb-49af-48b8-82d0-a8c0a827f290
ms.date: 4/26/2023
ms.keywords: IWMPDVD interface [Windows Media Player],resume method, IWMPDVD.resume, IWMPDVD::resume, IWMPDVDresume, resume, resume method [Windows Media Player], resume method [Windows Media Player],IWMPDVD interface, wmp.iwmpdvd_resume, wmp/IWMPDVD::resume
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Player 9 Series or later.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IWMPDVD::resume
 - wmp/IWMPDVD::resume
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
 - IWMPDVD.resume
---

# IWMPDVD::resume


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>resume</b> method returns to playback mode from menu mode at the same title position as when the menu was invoked.



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

<b>Windows Media Player 10 Mobile: </b>This method always returns S_OK, but does not perform the intended operation.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpdvd">IWMPDVD Interface</a>

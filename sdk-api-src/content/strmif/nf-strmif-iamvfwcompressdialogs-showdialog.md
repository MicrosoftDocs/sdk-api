---
UID: NF:strmif.IAMVfwCompressDialogs.ShowDialog
title: IAMVfwCompressDialogs::ShowDialog (strmif.h)
description: The ShowDialog method displays the specified dialog box.
helpviewer_keywords: ["IAMVfwCompressDialogs interface [DirectShow]","ShowDialog method","IAMVfwCompressDialogs.ShowDialog","IAMVfwCompressDialogs::ShowDialog","IAMVfwCompressDialogsShowDialog","ShowDialog","ShowDialog method [DirectShow]","ShowDialog method [DirectShow]","IAMVfwCompressDialogs interface","dshow.iamvfwcompressdialogs_showdialog","strmif/IAMVfwCompressDialogs::ShowDialog"]
old-location: dshow\iamvfwcompressdialogs_showdialog.htm
tech.root: dshow
ms.assetid: 4826bd47-0091-4a74-b88d-72a5b0f1c5ac
ms.date: 4/26/2023
ms.keywords: IAMVfwCompressDialogs interface [DirectShow],ShowDialog method, IAMVfwCompressDialogs.ShowDialog, IAMVfwCompressDialogs::ShowDialog, IAMVfwCompressDialogsShowDialog, ShowDialog, ShowDialog method [DirectShow], ShowDialog method [DirectShow],IAMVfwCompressDialogs interface, dshow.iamvfwcompressdialogs_showdialog, strmif/IAMVfwCompressDialogs::ShowDialog
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMVfwCompressDialogs::ShowDialog
 - strmif/IAMVfwCompressDialogs::ShowDialog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVfwCompressDialogs.ShowDialog
---

# IAMVfwCompressDialogs::ShowDialog


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ShowDialog</code> method displays the specified dialog box.

## -parameters

### -param iDialog [in]

Dialog box to display. This is a member of the <a href="/windows/desktop/api/strmif/ne-strmif-vfwcompressdialogs">VfwCompressDialogs</a> enumeration.

### -param hwnd [in]

Handle of the dialog box's parent window.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

This method returns an error when asked to display a dialog box while the driver is streaming or displaying another dialog box. While the driver displays the dialog box you can't stream (pause or run) the filter.

<code>IAMVfwCompressDialogs::ShowDialog</code> calls the Video for Windows video compression manager (VCM) functions <a href="/windows/desktop/api/vfw/nf-vfw-icconfigure">ICConfigure</a>, <a href="/windows/desktop/api/vfw/nf-vfw-icabout">ICAbout</a>, <a href="/windows/desktop/api/vfw/nf-vfw-icqueryconfigure">ICQueryConfigure</a>, and <a href="/windows/desktop/api/vfw/nf-vfw-icqueryabout">ICQueryAbout</a> to display the appropriate dialog box or determine if one exists.
      

The VfwCompressDialog_QueryConfig and VfwCompressDialog_QueryAbout members of the <a href="/windows/desktop/api/strmif/ne-strmif-vfwcompressdialogs">VfwCompressDialogs</a> enumeration tell you whether or not the configure dialog or about dialog is available. If passed one of these flags, the filter will return S_OK if the dialog exists, and S_FALSE if it does not. If a dialog is available, you call <code>ShowDialog</code> with the value VfwCompressDialog_Config or VfwCompressDialog_About to bring up the dialog.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvfwcompressdialogs">IAMVfwCompressDialogs Interface</a>
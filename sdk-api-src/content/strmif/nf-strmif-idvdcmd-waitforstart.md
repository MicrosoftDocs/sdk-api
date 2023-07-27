---
UID: NF:strmif.IDvdCmd.WaitForStart
title: IDvdCmd::WaitForStart (strmif.h)
description: The WaitForStart method blocks the DVD Navigator until the command associated with this object begins.
helpviewer_keywords: ["IDvdCmd interface [DirectShow]","WaitForStart method","IDvdCmd.WaitForStart","IDvdCmd::WaitForStart","IDvdCmdWaitForStart","WaitForStart","WaitForStart method [DirectShow]","WaitForStart method [DirectShow]","IDvdCmd interface","dshow.idvdcmd_waitforstart","strmif/IDvdCmd::WaitForStart"]
old-location: dshow\idvdcmd_waitforstart.htm
tech.root: dshow
ms.assetid: 7badcc93-b5e7-4f43-bd71-a0b9ddfb0053
ms.date: 4/26/2023
ms.keywords: IDvdCmd interface [DirectShow],WaitForStart method, IDvdCmd.WaitForStart, IDvdCmd::WaitForStart, IDvdCmdWaitForStart, WaitForStart, WaitForStart method [DirectShow], WaitForStart method [DirectShow],IDvdCmd interface, dshow.idvdcmd_waitforstart, strmif/IDvdCmd::WaitForStart
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdCmd::WaitForStart
 - strmif/IDvdCmd::WaitForStart
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
 - IDvdCmd.WaitForStart
---

# IDvdCmd::WaitForStart


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>WaitForStart</code> method blocks the DVD Navigator until the command associated with this object begins.



## -returns

Returns S_OK if successful or an <b>HRESULT</b> error code otherwise.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcmd">IDvdCmd Interface</a>



<a href="/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>

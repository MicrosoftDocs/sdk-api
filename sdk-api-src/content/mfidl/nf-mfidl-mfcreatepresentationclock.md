---
UID: NF:mfidl.MFCreatePresentationClock
title: MFCreatePresentationClock function (mfidl.h)
description: Creates the presentation clock.
helpviewer_keywords: ["MFCreatePresentationClock","MFCreatePresentationClock function [Media Foundation]","b0ed3482-d127-45d3-a4de-271b1c0a199b","mf.mfcreatepresentationclock","mfidl/MFCreatePresentationClock"]
old-location: mf\mfcreatepresentationclock.htm
tech.root: mf
ms.assetid: b0ed3482-d127-45d3-a4de-271b1c0a199b
ms.date: 12/05/2018
ms.keywords: MFCreatePresentationClock, MFCreatePresentationClock function [Media Foundation], b0ed3482-d127-45d3-a4de-271b1c0a199b, mf.mfcreatepresentationclock, mfidl/MFCreatePresentationClock
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreatePresentationClock
 - mfidl/MFCreatePresentationClock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreatePresentationClock
---

# MFCreatePresentationClock function


## -description

Creates the presentation clock. The presentation clock is used to schedule the time at which samples are rendered and to synchronize multiple streams.

## -parameters

### -param ppPresentationClock

Receives a pointer to the clock's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must shut down the presentation clock by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown">IMFShutdown::Shutdown</a> on the clock.

Typically applications do not create the presentation clock. The Media Session automatically creates the presentation clock. To get a pointer to the presentation clock from the Media Session, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock">IMFMediaSession::GetClock</a>.

## -see-also

<a href="/windows/desktop/medfound/about-the-media-session">About the Media Session</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
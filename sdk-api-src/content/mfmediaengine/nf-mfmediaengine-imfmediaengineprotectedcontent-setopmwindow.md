---
UID: NF:mfmediaengine.IMFMediaEngineProtectedContent.SetOPMWindow
title: IMFMediaEngineProtectedContent::SetOPMWindow (mfmediaengine.h)
description: Specifies the window that should receive output link protections.
helpviewer_keywords: ["IMFMediaEngineProtectedContent interface [Media Foundation]","SetOPMWindow method","IMFMediaEngineProtectedContent.SetOPMWindow","IMFMediaEngineProtectedContent::SetOPMWindow","SetOPMWindow","SetOPMWindow method [Media Foundation]","SetOPMWindow method [Media Foundation]","IMFMediaEngineProtectedContent interface","mf.imfmediaengineprotectedcontent_setopmwindow","mfmediaengine/IMFMediaEngineProtectedContent::SetOPMWindow"]
old-location: mf\imfmediaengineprotectedcontent_setopmwindow.htm
tech.root: mf
ms.assetid: 0102A98E-5EE0-4FBE-AF82-97C7A25038FB
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineProtectedContent interface [Media Foundation],SetOPMWindow method, IMFMediaEngineProtectedContent.SetOPMWindow, IMFMediaEngineProtectedContent::SetOPMWindow, SetOPMWindow, SetOPMWindow method [Media Foundation], SetOPMWindow method [Media Foundation],IMFMediaEngineProtectedContent interface, mf.imfmediaengineprotectedcontent_setopmwindow, mfmediaengine/IMFMediaEngineProtectedContent::SetOPMWindow
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaEngineProtectedContent::SetOPMWindow
 - mfmediaengine/IMFMediaEngineProtectedContent::SetOPMWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineProtectedContent.SetOPMWindow
---

# IMFMediaEngineProtectedContent::SetOPMWindow


## -description

Specifies the window that should receive output link protections.

## -parameters

### -param hwnd [in]

A handle to the window.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In frame-server mode, call this method to specify the destination window for protected video content. The Media Engine uses this window to set link protections, using the <a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a> (OPM).

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineprotectedcontent">IMFMediaEngineProtectedContent</a>
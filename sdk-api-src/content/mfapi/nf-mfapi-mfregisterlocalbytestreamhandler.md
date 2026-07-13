---
UID: NF:mfapi.MFRegisterLocalByteStreamHandler
title: MFRegisterLocalByteStreamHandler function (mfapi.h)
description: Registers a byte-stream handler in the caller's process.
helpviewer_keywords: ["MFRegisterLocalByteStreamHandler","MFRegisterLocalByteStreamHandler function [Media Foundation]","mf.mfregisterlocalbytestreamhandler","mfapi/MFRegisterLocalByteStreamHandler"]
old-location: mf\mfregisterlocalbytestreamhandler.htm
tech.root: mf
ms.assetid: B41FAA50-9CF7-4DD0-8571-1817C7C49276
ms.date: 12/05/2018
ms.keywords: MFRegisterLocalByteStreamHandler, MFRegisterLocalByteStreamHandler function [Media Foundation], mf.mfregisterlocalbytestreamhandler, mfapi/MFRegisterLocalByteStreamHandler
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFRegisterLocalByteStreamHandler
 - mfapi/MFRegisterLocalByteStreamHandler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFRegisterLocalByteStreamHandler
---

# MFRegisterLocalByteStreamHandler function


## -description

Registers a byte-stream handler in the caller's process.

## -parameters

### -param szFileExtension [in]

A string that contains the file name extension for this handler.

### -param szMimeType [in]

A string that contains the MIME type for this handler.

### -param pActivate [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface of an activation object. The caller implements this interface. The <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a> method of the activation object must create a byte-stream handler. The byte-stream handler exposes the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler">IMFByteStreamHandler</a> interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Byte-stream handlers are used in Microsoft Media Foundation during the source resolution process, which creates a media source from a URL. For more information, see <a href="/windows/desktop/medfound/scheme-handlers-and-byte-stream-handlers">Scheme Handlers and Byte-Stream Handlers</a>.

Within a process, local byte-stream handlers take precedence over byte-stream handlers that are registered in the registry. Local byte-stream handlers are not visible to other processes.

Use this function if you want to register a custom byte-stream handler for your application, but do not want the handler available to other applications.

Either <i>szFileExtension</i> or <i>szMimeType</i> can be <b>NULL</b>; at least one must be non-<b>NULL</b>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/scheme-handlers-and-byte-stream-handlers">Scheme Handlers and Byte-Stream Handlers</a>
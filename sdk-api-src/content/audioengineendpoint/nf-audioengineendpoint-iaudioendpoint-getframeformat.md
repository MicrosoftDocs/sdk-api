---
UID: NF:audioengineendpoint.IAudioEndpoint.GetFrameFormat
title: IAudioEndpoint::GetFrameFormat (audioengineendpoint.h)
description: Retrieves the format of the audio endpoint.
helpviewer_keywords: ["GetFrameFormat","GetFrameFormat method [Remote Desktop Services]","GetFrameFormat method [Remote Desktop Services]","IAudioEndpoint interface","IAudioEndpoint interface [Remote Desktop Services]","GetFrameFormat method","IAudioEndpoint.GetFrameFormat","IAudioEndpoint::GetFrameFormat","audioengineendpoint/IAudioEndpoint::GetFrameFormat","termserv.iaudioendpoint_getframeformat"]
old-location: termserv\iaudioendpoint_getframeformat.htm
tech.root: TermServ
ms.assetid: fb34ef19-4155-461e-a8d7-0a903e9d7c72
ms.date: 12/05/2018
ms.keywords: GetFrameFormat, GetFrameFormat method [Remote Desktop Services], GetFrameFormat method [Remote Desktop Services],IAudioEndpoint interface, IAudioEndpoint interface [Remote Desktop Services],GetFrameFormat method, IAudioEndpoint.GetFrameFormat, IAudioEndpoint::GetFrameFormat, audioengineendpoint/IAudioEndpoint::GetFrameFormat, termserv.iaudioendpoint_getframeformat
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
 - IAudioEndpoint::GetFrameFormat
 - audioengineendpoint/IAudioEndpoint::GetFrameFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioEndpoint.GetFrameFormat
---

# IAudioEndpoint::GetFrameFormat


## -description

The <b>GetFrameFormat</b> method retrieves the format of the audio endpoint.

## -parameters

### -param ppFormat [out]

Receives a pointer to a <b>WAVEFORMATEX</b> structure that contains the  format information for the device that the audio endpoint represents. The implementation must allocate memory for the structure by using <b>CoTaskMemAlloc</b>. The caller must free the buffer by using <b>CoTaskMemFree</b>. For information about <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>, see the Windows SDK documentation.

## -returns

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

This method must not be called from a real-time processing thread.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpoint">IAudioEndpoint</a>
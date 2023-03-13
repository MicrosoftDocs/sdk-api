---
UID: NF:shlobj.IThumbnailCapture.CaptureThumbnail
title: IThumbnailCapture::CaptureThumbnail (shlobj.h)
description: Retrieves a thumbnail representation of an IHTMLDocument2 document.
helpviewer_keywords: ["CaptureThumbnail","CaptureThumbnail method [Windows Shell]","CaptureThumbnail method [Windows Shell]","IThumbnailCapture interface","IThumbnailCapture interface [Windows Shell]","CaptureThumbnail method","IThumbnailCapture.CaptureThumbnail","IThumbnailCapture::CaptureThumbnail","_shell_IThumbnailCapture_CaptureThumbnail","shell.IThumbnailCapture_CaptureThumbnail","shlobj/IThumbnailCapture::CaptureThumbnail"]
old-location: shell\IThumbnailCapture_CaptureThumbnail.htm
tech.root: shell
ms.assetid: 3f492199-f40c-416f-b20f-84bd5c3b3709
ms.date: 08/02/2022
ms.keywords: CaptureThumbnail, CaptureThumbnail method [Windows Shell], CaptureThumbnail method [Windows Shell],IThumbnailCapture interface, IThumbnailCapture interface [Windows Shell],CaptureThumbnail method, IThumbnailCapture.CaptureThumbnail, IThumbnailCapture::CaptureThumbnail, _shell_IThumbnailCapture_CaptureThumbnail, shell.IThumbnailCapture_CaptureThumbnail, shlobj/IThumbnailCapture::CaptureThumbnail
req.header: shlobj.h
req.include-header: 
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
req.lib: 
req.dll: Shimgvw.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IThumbnailCapture::CaptureThumbnail
 - shlobj/IThumbnailCapture::CaptureThumbnail
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shimgvw.dll
api_name:
 - IThumbnailCapture.CaptureThumbnail
---

# IThumbnailCapture::CaptureThumbnail


## -description

Retrieves a thumbnail representation of an <a href="/dotnet/api/mshtml.ihtmldocument2?view=powershellsdk-1.1.0&preserve-view=true">IHTMLDocument2</a> document.
        
            
<div class="alert"><b>Note</b>  This method is deprecated as of Windows 7. The feature it supported is no longer present in Windows.</div><div> </div>

## -parameters

### -param pMaxSize [in]

Type: <b>const <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>*</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that specifies the maximum size of the bitmap, in pixels.

### -param pHTMLDoc2 [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an <a href="/dotnet/api/mshtml.ihtmldocument2?view=powershellsdk-1.1.0&preserve-view=true">IHTMLDocument2</a> interface's <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

### -param phbmThumbnail [out]

Type: <b>HBITMAP*</b>

A handle to a bitmap that represents the document object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/dotnet/api/mshtml.ihtmldocument2?view=powershellsdk-1.1.0&preserve-view=true">IHTMLDocument2</a>



<a href="/windows/desktop/api/shlobj/nn-shlobj-ithumbnailcapture">IThumbnailCapture</a>
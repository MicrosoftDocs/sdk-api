---
UID: NF:shlobj.IThumbnailCapture.CaptureThumbnail
title: IThumbnailCapture::CaptureThumbnail
author: windows-sdk-content
description: Retrieves a thumbnail representation of an IHTMLDocument2 document.
old-location: shell\IThumbnailCapture_CaptureThumbnail.htm
tech.root: shell
ms.assetid: 3f492199-f40c-416f-b20f-84bd5c3b3709
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: CaptureThumbnail, CaptureThumbnail method [Windows Shell], CaptureThumbnail method [Windows Shell],IThumbnailCapture interface, IThumbnailCapture interface [Windows Shell],CaptureThumbnail method, IThumbnailCapture.CaptureThumbnail, IThumbnailCapture::CaptureThumbnail, _shell_IThumbnailCapture_CaptureThumbnail, shell.IThumbnailCapture_CaptureThumbnail, shlobj/IThumbnailCapture::CaptureThumbnail
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shimgvw.dll
api_name:
 - IThumbnailCapture.CaptureThumbnail
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IThumbnailCapture::CaptureThumbnail


## -description


Retrieves a thumbnail representation of an <a href="https://msdn.microsoft.com/d713c045-ab50-465d-96b6-a20c40093f97">IHTMLDocument2</a> document.
        
            
<div class="alert"><b>Note</b>  This method is deprecated as of Windows 7. The feature it supported is no longer present in Windows.</div><div> </div>

## -parameters




### -param pMaxSize [in]

Type: <b>const <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that specifies the maximum size of the bitmap, in pixels.


### -param pHTMLDoc2 [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/d713c045-ab50-465d-96b6-a20c40093f97">IHTMLDocument2</a> interface's <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.


### -param phbmThumbnail [out]

Type: <b>HBITMAP*</b>

A handle to a bitmap that represents the document object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d713c045-ab50-465d-96b6-a20c40093f97">IHTMLDocument2</a>



<a href="https://msdn.microsoft.com/fecf1f8f-ea76-4a3d-a6cf-faa3e400f5e4">IThumbnailCapture</a>
 

 


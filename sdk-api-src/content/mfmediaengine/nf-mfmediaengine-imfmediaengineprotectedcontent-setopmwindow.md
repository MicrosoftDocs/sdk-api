---
UID: NF:mfmediaengine.IMFMediaEngineProtectedContent.SetOPMWindow
title: IMFMediaEngineProtectedContent::SetOPMWindow
author: windows-sdk-content
description: Specifies the window that should receive output link protections.
old-location: mf\imfmediaengineprotectedcontent_setopmwindow.htm
tech.root: medfound
ms.assetid: 0102A98E-5EE0-4FBE-AF82-97C7A25038FB
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: IMFMediaEngineProtectedContent interface [Media Foundation],SetOPMWindow method, IMFMediaEngineProtectedContent.SetOPMWindow, IMFMediaEngineProtectedContent::SetOPMWindow, SetOPMWindow, SetOPMWindow method [Media Foundation], SetOPMWindow method [Media Foundation],IMFMediaEngineProtectedContent interface, mf.imfmediaengineprotectedcontent_setopmwindow, mfmediaengine/IMFMediaEngineProtectedContent::SetOPMWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineProtectedContent.SetOPMWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineProtectedContent::SetOPMWindow


## -description


Specifies the window that should receive output link protections.


## -parameters




### -param hwnd [in]

A handle to the window.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In frame-server mode, call this method to specify the destination window for protected video content. The Media Engine uses this window to set link protections, using the <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a> (OPM).




## -see-also




<a href="https://msdn.microsoft.com/85B37711-DB46-4BC7-A051-79E9507791FA">IMFMediaEngineProtectedContent</a>
 

 


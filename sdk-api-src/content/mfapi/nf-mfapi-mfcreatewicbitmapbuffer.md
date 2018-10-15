---
UID: NF:mfapi.MFCreateWICBitmapBuffer
title: MFCreateWICBitmapBuffer function
author: windows-sdk-content
description: Creates a media buffer object that manages a Windows Imaging Component (WIC).
old-location: mf\mfcreatewicbitmapbuffer.htm
tech.root: medfound
ms.assetid: 029B7CC6-5B12-4A19-B6CD-B0D7E3F314B6
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: MFCreateWICBitmapBuffer, MFCreateWICBitmapBuffer function [Media Foundation], mf.mfcreatewicbitmapbuffer, mfapi/MFCreateWICBitmapBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateWICBitmapBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateWICBitmapBuffer function


## -description


Creates a media buffer object that manages a Windows Imaging Component (WIC) bitmap.


## -parameters




### -param riid [in]

Set this parameter to <code>__uuidof(IWICBitmap)</code>.


### -param punkSurface [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the bitmap surface. The bitmap surface must be a WIC bitmap that exposes the <a href="https://msdn.microsoft.com/15dcc80d-ef58-453d-a57a-348ffc7ddc6b">IWICBitmap</a> interface.


### -param ppBuffer [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 


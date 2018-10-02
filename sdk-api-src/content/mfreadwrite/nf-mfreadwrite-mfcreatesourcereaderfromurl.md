---
UID: NF:mfreadwrite.MFCreateSourceReaderFromURL
title: MFCreateSourceReaderFromURL function
author: windows-sdk-content
description: Creates the source reader from a URL.
old-location: mf\mfcreatesourcereaderfromurl.htm
tech.root: MedFound
ms.assetid: 060b4ab3-9a9f-4c90-a8c5-9c6d81877e2f
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MFCreateSourceReaderFromURL, MFCreateSourceReaderFromURL function [Media Foundation], mf.mfcreatesourcereaderfromurl, mfreadwrite/MFCreateSourceReaderFromURL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfreadwrite.lib
req.dll: Mfreadwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfreadwrite.dll
api_name:
 - MFCreateSourceReaderFromURL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateSourceReaderFromURL function


## -description


Creates the source reader from a URL.


## -parameters




### -param pwszURL [in]

The URL  of a media file to open.


### -param pAttributes [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. You can use this parameter to configure the source reader. For more information, see <a href="https://msdn.microsoft.com/312a588a-848b-4563-893a-fac49a4ca465">Source Reader Attributes</a>. This parameter can be <b>NULL</b>.


### -param ppSourceReader [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call <b>CoInitialize(Ex)</b> and <a href="https://msdn.microsoft.com/b4472e40-3681-4b26-9385-4df7bf19c2d8">MFStartup</a> before calling this function.

Internally, the source reader calls the <a href="https://msdn.microsoft.com/b8f751b1-6456-4d67-839d-ecfa388e8d71">IMFSourceResolver::CreateObjectFromURL</a> method to create a media source from the URL.
      

This function is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>
 

 


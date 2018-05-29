---
UID: NF:mfreadwrite.MFCreateSourceReaderFromByteStream
title: MFCreateSourceReaderFromByteStream function
author: windows-sdk-content
description: Creates the source reader from a byte stream.
old-location: mf\mfcreatesourcereaderfrombytestream.htm
old-project: medfound
ms.assetid: e167159d-902c-4c34-b5f0-eb764fe2de1c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MFCreateSourceReaderFromByteStream, MFCreateSourceReaderFromByteStream function [Media Foundation], mf.mfcreatesourcereaderfrombytestream, mfreadwrite/MFCreateSourceReaderFromByteStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfreadwrite.dll
api_name:
-	MFCreateSourceReaderFromByteStream
product: Windows
targetos: Windows
req.lib: Mfreadwrite.lib
req.dll: Mfreadwrite.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateSourceReaderFromByteStream function


## -description


Creates the source reader from a byte stream.


## -parameters




### -param pByteStream [in]

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of a byte stream. This byte stream will provide the source data for the source reader.


### -param pAttributes [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. You can use this parameter to configure the source reader. For more information, see <a href="https://msdn.microsoft.com/312a588a-848b-4563-893a-fac49a4ca465">Source Reader Attributes</a>. This parameter can be <b>NULL</b>.


### -param ppSourceReader [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call <b>CoInitialize(Ex)</b> and <a href="https://msdn.microsoft.com/b4472e40-3681-4b26-9385-4df7bf19c2d8">MFStartup</a> before calling this function.


        
        Internally, the source reader calls the <a href="https://msdn.microsoft.com/e4a4aad5-0924-4251-b0da-6919ae010bf0">IMFSourceResolver::CreateObjectFromByteStream</a> method to create a media source from the byte stream. Therefore, a byte-stream handler must be registered for the byte stream. For more information about byte-stream handlers, see <a href="https://msdn.microsoft.com/b0113527-f22c-4519-b1cf-fea54bff4090">Scheme Handlers and Byte-Stream Handlers</a>.
      

This function is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>
 

 


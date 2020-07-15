---
UID: NF:mfreadwrite.MFCreateSourceReaderFromURL
title: MFCreateSourceReaderFromURL function (mfreadwrite.h)
description: Creates the source reader from a URL.
helpviewer_keywords: ["MFCreateSourceReaderFromURL","MFCreateSourceReaderFromURL function [Media Foundation]","mf.mfcreatesourcereaderfromurl","mfreadwrite/MFCreateSourceReaderFromURL"]
old-location: mf\mfcreatesourcereaderfromurl.htm
tech.root: medfound
ms.assetid: 060b4ab3-9a9f-4c90-a8c5-9c6d81877e2f
ms.date: 12/05/2018
ms.keywords: MFCreateSourceReaderFromURL, MFCreateSourceReaderFromURL function [Media Foundation], mf.mfcreatesourcereaderfromurl, mfreadwrite/MFCreateSourceReaderFromURL
f1_keywords:
- mfreadwrite/MFCreateSourceReaderFromURL
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateSourceReaderFromURL function


## -description


Creates the source reader from a URL.


## -parameters




### -param pwszURL [in]

The URL  of a media file to open.


### -param pAttributes [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. You can use this parameter to configure the source reader. For more information, see <a href="https://docs.microsoft.com/windows/desktop/medfound/source-reader-attributes">Source Reader Attributes</a>. This parameter can be <b>NULL</b>.


### -param ppSourceReader [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call <b>CoInitialize(Ex)</b> and <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a> before calling this function.

Internally, the source reader calls the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl">IMFSourceResolver::CreateObjectFromURL</a> method to create a media source from the URL.
      

This function is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/source-reader">Source Reader</a>
 

 


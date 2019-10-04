---
UID: NF:mfapi.MFCreateMediaType
title: MFCreateMediaType function (mfapi.h)
author: windows-sdk-content
description: Creates an empty media type.
old-location: mf\mfcreatemediatype.htm
tech.root: medfound
ms.assetid: 05b0941e-03ce-4ced-9022-22b65d1c4b4c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 05b0941e-03ce-4ced-9022-22b65d1c4b4c, MFCreateMediaType, MFCreateMediaType function [Media Foundation], mf.mfcreatemediatype, mfapi/MFCreateMediaType
ms.topic: function
f1_keywords: 
 - "mfapi/MFCreateMediaType"
dev_langs:
 - c++
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - MFCreateMediaType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateMediaType function


## -description



Creates an empty media type.




## -parameters




### -param ppMFType

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The media type is created without any attributes.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-types">Media Types</a>
 

 


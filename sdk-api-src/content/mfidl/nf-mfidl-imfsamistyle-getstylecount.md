---
UID: NF:mfidl.IMFSAMIStyle.GetStyleCount
title: IMFSAMIStyle::GetStyleCount (mfidl.h)
description: Gets the number of styles defined in the SAMI file.
helpviewer_keywords: ["161cd457-9fab-4ebb-b8b8-f87326d67c66","GetStyleCount","GetStyleCount method [Media Foundation]","GetStyleCount method [Media Foundation]","IMFSAMIStyle interface","IMFSAMIStyle interface [Media Foundation]","GetStyleCount method","IMFSAMIStyle.GetStyleCount","IMFSAMIStyle::GetStyleCount","mf.imfsamistyle_getstylecount","mfidl/IMFSAMIStyle::GetStyleCount"]
old-location: mf\imfsamistyle_getstylecount.htm
tech.root: mf
ms.assetid: 161cd457-9fab-4ebb-b8b8-f87326d67c66
ms.date: 12/05/2018
ms.keywords: 161cd457-9fab-4ebb-b8b8-f87326d67c66, GetStyleCount, GetStyleCount method [Media Foundation], GetStyleCount method [Media Foundation],IMFSAMIStyle interface, IMFSAMIStyle interface [Media Foundation],GetStyleCount method, IMFSAMIStyle.GetStyleCount, IMFSAMIStyle::GetStyleCount, mf.imfsamistyle_getstylecount, mfidl/IMFSAMIStyle::GetStyleCount
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSAMIStyle::GetStyleCount
 - mfidl/IMFSAMIStyle::GetStyleCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSAMIStyle.GetStyleCount
---

# IMFSAMIStyle::GetStyleCount


## -description

Gets the number of styles defined in the SAMI file.

## -parameters

### -param pdwCount [out]

Receives the number of SAMI styles in the file.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle">IMFSAMIStyle</a>



<a href="/windows/desktop/medfound/sami-media-source">SAMI Media Source</a>
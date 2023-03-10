---
UID: NF:windows.graphics.imaging.interop.ISoftwareBitmapNative.GetData
title: ISoftwareBitmapNative::imaging (windows.graphics.imaging.interop.h)
description: This method returns an interface that provides access to the software bitmap data.
helpviewer_keywords: ["GetData","GetData method [Windows Runtime]","GetData method [Windows Runtime]","ISoftwareBitmapNative interface","ISoftwareBitmapNative interface [Windows Runtime]","GetData method","ISoftwareBitmapNative.GetData","ISoftwareBitmapNative.imaging","ISoftwareBitmapNative::GetData","ISoftwareBitmapNative::imaging","windows/ISoftwareBitmapNative::GetData","winrt.isoftwarebitmapnative_getdata"]
old-location: winrt\isoftwarebitmapnative_getdata.htm
tech.root: WinRT
ms.assetid: 4BB9674A-A95A-4183-A1E1-428AB140D6EB
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [Windows Runtime], GetData method [Windows Runtime],ISoftwareBitmapNative interface, ISoftwareBitmapNative interface [Windows Runtime],GetData method, ISoftwareBitmapNative.GetData, ISoftwareBitmapNative.imaging, ISoftwareBitmapNative::GetData, ISoftwareBitmapNative::imaging, windows/ISoftwareBitmapNative::GetData, winrt.isoftwarebitmapnative_getdata
req.header: windows.graphics.imaging.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windows.graphics.imaging.interop.lib
req.dll: Windows.graphics.imaging.interop.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISoftwareBitmapNative::GetData
 - windows.graphics.imaging.interop/ISoftwareBitmapNative::GetData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.graphics.imaging.interop.dll
api_name:
 - ISoftwareBitmapNative.GetData
---

# ISoftwareBitmapNative::imaging


## -description

This method returns an interface that provides access to the software bitmap data.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

The IID of the interface to retrieve.

### -param ppv

Type: <b>LPVOID*</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i> parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK on successful completion. Returns E_NOINTERFACE if the requested interface can't be found.

## -see-also

<a href="/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnative">ISoftwareBitmapNative</a>
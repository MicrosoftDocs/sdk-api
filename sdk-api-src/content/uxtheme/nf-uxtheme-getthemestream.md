---
UID: NF:uxtheme.GetThemeStream
title: GetThemeStream function (uxtheme.h)
description: Retrieves a data stream corresponding to a specified theme, starting from a specified part, state, and property.
helpviewer_keywords: ["GetThemeStream","GetThemeStream function [Windows Controls]","controls.GetThemeStream","controls.inet_GetThemeStream","inet_GetThemeStream","inet_GetThemeStream_cpp","uxtheme/GetThemeStream"]
old-location: controls\GetThemeStream.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemestream.htm
ms.date: 12/05/2018
ms.keywords: GetThemeStream, GetThemeStream function [Windows Controls], controls.GetThemeStream, controls.inet_GetThemeStream, inet_GetThemeStream, inet_GetThemeStream_cpp, uxtheme/GetThemeStream
req.header: uxtheme.h
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
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetThemeStream
 - uxtheme/GetThemeStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-uxtheme-themes-l1-1-3.dll
 - ext-ms-win-uxtheme-themes-l1-1-2.dll
 - UxTheme.dll
api_name:
 - GetThemeStream
---

# GetThemeStream function


## -description

Retrieves a data stream corresponding to a specified theme, starting from a specified part, state, and property.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to the theme from which the stream will be retrieved.

### -param iPartId [in]

Type: <b>int</b>

Specifies the part to retrieve a stream from. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Specifies the state of the part.

### -param iPropId [in]

Type: <b>int</b>

Specifies the property to retrieve.

### -param ppvStream [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">VOID</a>**</b>

Address of a pointer that receives the stream.

### -param pcbStream [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

Pointer that receives the length, in bytes, of the stream received by <i>ppvStream</i>.

### -param hInst [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

If <i>iPropId</i> is TMT_STREAM, this value is <b>NULL</b>. If <i>iPropId</i> is TMT_DISKSTREAM, this value is the HINSTANCE of a loaded styles file.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Windows 8:</b> In high contrast mode, the data stream retrieved by this function is not valid after the <i>hTheme</i> theme handle is closed.


The data stream retrieved by this function is not a copy; do not delete or close the data stream after using it.

## -see-also

<a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>
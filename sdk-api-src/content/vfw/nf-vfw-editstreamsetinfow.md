---
UID: NF:vfw.EditStreamSetInfoW
title: EditStreamSetInfoW function (vfw.h)
description: The EditStreamSetInfo function changes characteristics of an editable stream. (Unicode)
helpviewer_keywords: ["EditStreamSetInfo", "EditStreamSetInfo function [Windows Multimedia]", "EditStreamSetInfoW", "_win32_EditStreamSetInfo", "multimedia.editstreamsetinfo", "vfw/EditStreamSetInfo", "vfw/EditStreamSetInfoW"]
old-location: multimedia\editstreamsetinfo.htm
tech.root: Multimedia
ms.assetid: c9b33a91-b7b1-4b66-86ba-d1ea774c8743
ms.date: 12/05/2018
ms.keywords: EditStreamSetInfo, EditStreamSetInfo function [Windows Multimedia], EditStreamSetInfoA, EditStreamSetInfoW, _win32_EditStreamSetInfo, multimedia.editstreamsetinfo, vfw/EditStreamSetInfo, vfw/EditStreamSetInfoA, vfw/EditStreamSetInfoW
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EditStreamSetInfoW (Unicode) and EditStreamSetInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EditStreamSetInfoW
 - vfw/EditStreamSetInfoW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
api_name:
 - EditStreamSetInfo
 - EditStreamSetInfoA
 - EditStreamSetInfoW
---

# EditStreamSetInfoW function


## -description

The <b>EditStreamSetInfo</b> function changes characteristics of an editable stream.

## -parameters

### -param pavi

Handle to an open stream.

### -param lpInfo

Pointer to an <a href="/windows/desktop/api/vfw/ns-vfw-avistreaminfoa">AVISTREAMINFO</a> structure containing new information.

### -param cbInfo

Size, in bytes, of the structure pointed to by <i>lpInfo</i>.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

You must supply information for the entire <a href="/windows/desktop/api/vfw/ns-vfw-avistreaminfoa">AVISTREAMINFO</a> structure, including the members you will not use. You can use the <a href="/windows/desktop/api/vfw/nf-vfw-avistreaminfoa">AVIStreamInfo</a> function to initialize the structure and then update selected members with your data.

This function does not change the following members:

<ul>
<li><b>dwCaps</b></li>
<li><b>dwEditCount</b></li>
<li><b>dwFlags</b></li>
<li><b>dwInitialFrames</b></li>
<li><b>dwLength</b></li>
<li><b>dwSampleSize</b></li>
<li><b>dwSuggestedBufferSize</b></li>
<li><b>fccHandler</b></li>
<li><b>fccType</b></li>
</ul>
The function changes the following members:

<ul>
<li><b>dwRate</b></li>
<li><b>dwQuality</b></li>
<li><b>dwScale</b></li>
<li><b>dwStart</b></li>
<li><b>rcFrame</b></li>
<li><b>szName</b></li>
<li><b>wLanguage</b></li>
<li><b>wPriority</b></li>
</ul>




> [!NOTE]
> The vfw.h header defines EditStreamSetInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>

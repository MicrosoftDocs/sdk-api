---
UID: NF:vfw.EditStreamSetNameA
title: EditStreamSetNameA function (vfw.h)
description: The EditStreamSetName function assigns a descriptive string to a stream. (ANSI)
helpviewer_keywords: ["EditStreamSetNameA", "vfw/EditStreamSetNameA"]
old-location: multimedia\editstreamsetname.htm
tech.root: Multimedia
ms.assetid: 33542ad1-4bee-4051-8b75-f5328086250b
ms.date: 12/05/2018
ms.keywords: EditStreamSetName, EditStreamSetName function [Windows Multimedia], EditStreamSetNameA, EditStreamSetNameW, _win32_EditStreamSetName, multimedia.editstreamsetname, vfw/EditStreamSetName, vfw/EditStreamSetNameA, vfw/EditStreamSetNameW
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EditStreamSetNameW (Unicode) and EditStreamSetNameA (ANSI)
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
 - EditStreamSetNameA
 - vfw/EditStreamSetNameA
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
 - EditStreamSetName
 - EditStreamSetNameA
 - EditStreamSetNameW
---

# EditStreamSetNameA function


## -description

The <b>EditStreamSetName</b> function assigns a descriptive string to a stream.

## -parameters

### -param pavi

Handle to an open stream.

### -param lpszName

Null-terminated string containing the description of the stream.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

This function updates the <b>szName</b> member of the <b>AVISTREAMINFO</b> structure.





> [!NOTE]
> The vfw.h header defines EditStreamSetName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>

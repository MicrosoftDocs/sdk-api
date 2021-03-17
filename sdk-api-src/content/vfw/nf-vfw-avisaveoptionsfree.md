---
UID: NF:vfw.AVISaveOptionsFree
title: AVISaveOptionsFree function (vfw.h)
description: The AVISaveOptionsFree function frees the resources allocated by the AVISaveOptions function.
helpviewer_keywords: ["AVISaveOptionsFree","AVISaveOptionsFree function [Windows Multimedia]","_win32_AVISaveOptionsFree","multimedia.avisaveoptionsfree","vfw/AVISaveOptionsFree"]
old-location: multimedia\avisaveoptionsfree.htm
tech.root: Multimedia
ms.assetid: c88a786f-d008-4eb6-af3d-59a0f62ac09d
ms.date: 12/05/2018
ms.keywords: AVISaveOptionsFree, AVISaveOptionsFree function [Windows Multimedia], _win32_AVISaveOptionsFree, multimedia.avisaveoptionsfree, vfw/AVISaveOptionsFree
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - AVISaveOptionsFree
 - vfw/AVISaveOptionsFree
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
 - AVISaveOptionsFree
---

# AVISaveOptionsFree function


## -description

The <b>AVISaveOptionsFree</b> function frees the resources allocated by the <a href="/windows/desktop/api/vfw/nf-vfw-avisaveoptions">AVISaveOptions</a> function.

## -parameters

### -param nStreams

Count of the <a href="/windows/desktop/api/vfw/ns-vfw-avicompressoptions">AVICOMPRESSOPTIONS</a> structures referenced in <i>plpOptions</i>.

### -param plpOptions

Pointer to an array of pointers to <a href="/windows/desktop/api/vfw/ns-vfw-avicompressoptions">AVICOMPRESSOPTIONS</a> structures. These structures hold the compression options set by the dialog box. The resources allocated by <a href="/windows/desktop/api/vfw/nf-vfw-avisaveoptions">AVISaveOptions</a> for each of these structures will be freed.

## -returns

Returns AVIERR_OK.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>
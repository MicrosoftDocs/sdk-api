---
UID: NF:imagehlp.MapFileAndCheckSumW
title: MapFileAndCheckSumW function (imagehlp.h)
description: Computes the checksum of the specified file. (Unicode)
helpviewer_keywords: ["MapFileAndCheckSum", "MapFileAndCheckSum function", "MapFileAndCheckSumW", "_win32_mapfileandchecksum", "base.mapfileandchecksum", "imagehlp/MapFileAndCheckSum", "imagehlp/MapFileAndCheckSumW"]
old-location: base\mapfileandchecksum.htm
tech.root: Debug
ms.assetid: e8fac3cc-bddf-419d-a245-d7af84d2c7f7
ms.date: 12/05/2018
ms.keywords: MapFileAndCheckSum, MapFileAndCheckSum function, MapFileAndCheckSumA, MapFileAndCheckSumW, _win32_mapfileandchecksum, base.mapfileandchecksum, imagehlp/MapFileAndCheckSum, imagehlp/MapFileAndCheckSumA, imagehlp/MapFileAndCheckSumW
req.header: imagehlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MapFileAndCheckSumW (Unicode) and MapFileAndCheckSumA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Imagehlp.lib
req.dll: Imagehlp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MapFileAndCheckSumW
 - imagehlp/MapFileAndCheckSumW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imagehlp.dll
api_name:
 - MapFileAndCheckSum
 - MapFileAndCheckSumA
 - MapFileAndCheckSumW
---

# MapFileAndCheckSumW function


## -description

Computes the checksum of the specified file.

## -parameters

### -param Filename [in]

The file name of the file for which the checksum is to be computed.

### -param HeaderSum [out]

A pointer to a variable that receives the original checksum from the image file, or zero if there is an error.

### -param CheckSum [out]

A pointer to a variable that receives the computed checksum.

## -returns

If the function succeeds, the return value is CHECKSUM_SUCCESS (0).

If the function fails, the return value is one of the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CHECKSUM_MAP_FAILURE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Could not map the file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CHECKSUM_MAPVIEW_FAILURE</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Could not map a view of the file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CHECKSUM_OPEN_FAILURE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Could not open the file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CHECKSUM_UNICODE_FAILURE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Could not convert the file name to Unicode.

</td>
</tr>
</table>

## -remarks

The 
<b>MapFileAndCheckSum</b> function computes a new checksum for the file and returns it in the <i>CheckSum</i> parameter. This function is used by any application that creates or modifies an executable image. Checksums are required for kernel-mode drivers and some system DLLs. The linker computes the original checksum at link time, if you use the appropriate linker switch. For more details, see your linker documentation.

It is recommended that all images have valid checksums. It is the caller's responsibility to place the newly computed checksum into the mapped image and update the on-disk image of the file.

Passing a <i>Filename</i> parameter that does not point to a valid executable image will produce unpredictable results.  Any user of this function is encouraged to make sure that a valid executable image is being passed.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

<div class="alert"><b>Note</b>  The Unicode implementation of this function calls the ASCII implementation and as a result, the function can fail if the codepage does not support the characters in the path. For example, if you pass a non-English Unicode file path, and the default codepage is English, the unrecognized non-English wide chars are converted to "??" and the file cannot be opened (the function returns CHECKSUM_OPEN_FAILURE).</div>
<div> </div>




> [!NOTE]
> The imagehlp.h header defines MapFileAndCheckSum as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/imagehlp/nf-imagehlp-checksummappedfile">CheckSumMappedFile</a>



<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>

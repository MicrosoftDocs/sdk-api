---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



## -see-also




<a href="https://msdn.microsoft.com/01a99601-64de-412d-991e-b1708286ca8c">CheckSumMappedFile</a>



<a href="https://msdn.microsoft.com/926f412e-25ba-4f9c-a118-b5a1bc723379">ImageHlp Functions</a>
 

 


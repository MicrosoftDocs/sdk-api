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

# AVISaveOptions function


## -description



The <b>AVISaveOptions</b> function retrieves the save options for a file and returns them in a buffer.




## -parameters




### -param hwnd

Handle to the parent window for the Compression Options dialog box.


### -param uiFlags

Flags for displaying the Compression Options dialog box. The following flags are defined.

<table>
<tr>
<th>
Value
</th>
<th>
Meaning
</th>
</tr>
<tr>
<td>ICMF_CHOOSE_KEYFRAME</td>
<td>Displays a Key Frame Every dialog box for the video options. This is the same flag used in the <a href="https://msdn.microsoft.com/4a58df6a-9ac4-44bb-8c49-338bb60193fc">ICCompressorChoose</a> function.</td>
</tr>
<tr>
<td>ICMF_CHOOSE_DATARATE</td>
<td>Displays a Data Rate dialog box for the video options. This is the same flag used in <a href="https://msdn.microsoft.com/4a58df6a-9ac4-44bb-8c49-338bb60193fc">ICCompressorChoose</a>.</td>
</tr>
<tr>
<td>ICMF_CHOOSE_PREVIEW</td>
<td>Displays a Preview button for the video options. This button previews the compression by using a frame from the stream. This is the same flag used in <a href="https://msdn.microsoft.com/4a58df6a-9ac4-44bb-8c49-338bb60193fc">ICCompressorChoose</a>.</td>
</tr>
</table>
 


### -param nStreams


            Number of streams that have their options set by the dialog box.
          


### -param ppavi


            Pointer to an array of stream interface pointers. The <i>nStreams</i> parameter indicates the number of pointers in the array.
          


### -param plpOptions

Pointer to an array of pointers to <a href="https://msdn.microsoft.com/8084adc3-792f-4a6c-b407-51e0e435e629">AVICOMPRESSOPTIONS</a> structures. These structures hold the compression options set by the dialog box. The <i>nStreams</i> parameter indicates the number of pointers in the array.


## -returns



Returns <b>TRUE</b> if the user pressed OK, <b>FALSE</b> for CANCEL, or an error otherwise.




## -remarks



This function presents a standard Compression Options dialog box using <i>hwnd</i> as the parent window handle. When the user is finished selecting the compression options for each stream, the options are returned in the <a href="https://msdn.microsoft.com/8084adc3-792f-4a6c-b407-51e0e435e629">AVICOMPRESSOPTIONS</a> structure in the array referenced by <i>plpOptions</i>. The calling application must pass the interface pointers for the streams in the array referenced by <i>ppavi</i>.

An application must allocate memory for the <a href="https://msdn.microsoft.com/8084adc3-792f-4a6c-b407-51e0e435e629">AVICOMPRESSOPTIONS</a> structures and the array of pointers to these structures.

The argument <i>ppavi</i> contains the address of a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 


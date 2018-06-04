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

# ICInstall function


## -description



The <b>ICInstall</b> function installs a new compressor or decompressor.




## -parameters




### -param fccType

Four-character code indicating the type of data used by the compressor or decompressor. Specify "VIDC" for a video compressor or decompressor.


### -param fccHandler

Four-character code identifying a specific compressor or decompressor.


### -param lParam

Pointer to a null-terminated string containing the name of the compressor or decompressor, or the address of a function used for compression or decompression. The contents of this parameter are defined by the flags set for <i>wFlags</i>.


### -param szDesc

Reserved; do not use.


### -param wFlags

Flags defining the contents of <i>lParam</i>. The following values are defined.

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
<td>ICINSTALL_DRIVER</td>
<td>The <i>lParam</i> parameter contains the address of a null-terminated string that names the compressor to install.</td>
</tr>
<tr>
<td>ICINSTALL_FUNCTION</td>
<td>The <i>lParam</i> parameter contains the address of a compressor function. This function should be structured like the <a href="https://msdn.microsoft.com/d9a5535f-6b80-40cc-a20b-b7a342414d7f">DriverProc</a> entry point function used by compressors.</td>
</tr>
</table>
 


## -returns



Returns ICERR_OK if successful or an error otherwise.




## -remarks



Applications must open an installed compressor or decompressor before using it.

If your application installs a function as a compressor or decompressor, it should remove the function with the <a href="https://msdn.microsoft.com/c5f2638a-6b75-4e30-8420-94011c73f5bd">ICRemove</a> function before it terminates. This prevents other applications from trying to access the function when it is not available.




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 


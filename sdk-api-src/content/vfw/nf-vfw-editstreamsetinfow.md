---
UID: NF:vfw.EditStreamSetInfoW
title: EditStreamSetInfoW function
author: windows-sdk-content
description: The EditStreamSetInfo function changes characteristics of an editable stream.
old-location: multimedia\editstreamsetinfo.htm
old-project: Multimedia
ms.assetid: c9b33a91-b7b1-4b66-86ba-d1ea774c8743
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EditStreamSetInfo, EditStreamSetInfo function [Windows Multimedia], EditStreamSetInfoA, EditStreamSetInfoW, _win32_EditStreamSetInfo, multimedia.editstreamsetinfo, vfw/EditStreamSetInfo, vfw/EditStreamSetInfoA, vfw/EditStreamSetInfoW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
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
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
req.product: Windows UI
---

# EditStreamSetInfoW function


## -description



The <b>EditStreamSetInfo</b> function changes characteristics of an editable stream.




## -parameters




### -param pavi

Handle to an open stream.


### -param lpInfo

Pointer to an <a href="https://msdn.microsoft.com/dca6d9ca-a825-4bd0-a19d-0655d775fdfb">AVISTREAMINFO</a> structure containing new information.


### -param cbInfo

Size, in bytes, of the structure pointed to by <i>lpInfo</i>.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



You must supply information for the entire <a href="https://msdn.microsoft.com/dca6d9ca-a825-4bd0-a19d-0655d775fdfb">AVISTREAMINFO</a> structure, including the members you will not use. You can use the <a href="https://msdn.microsoft.com/7a1ba29b-e8ba-435d-a551-c9184631971c">AVIStreamInfo</a> function to initialize the structure and then update selected members with your data.

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



## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 


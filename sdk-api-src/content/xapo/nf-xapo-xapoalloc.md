---
UID: NF:xapo.XAPOAlloc
title: XAPOAlloc macro
author: windows-sdk-content
description: Memory allocation macro used by IXAPO methods that must allocate arbitrary sized structures that are subsequently returned to the application.
old-location: xaudio2\xapoalloc.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xapo.XAPOAlloc(ULONG)
ms.author: windowssdkdev
ms.date: 04/23/2018
ms.keywords: XAPOAlloc, XAPOAlloc macro [XAudio2 Audio Mixing APIs], xapo/XAPOAlloc, xaudio2.xapoalloc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: xapo.h
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
tech.root: 
req.typenames: XAPO_BUFFER_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - XAPO.h
api_name:
 - XAPOAlloc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# XAPOAlloc macro


## -description


Memory allocation macro used by IXAPO methods that must allocate arbitrary sized structures that are subsequently returned to the application.


## -parameters




### -param size

Size, in bytes, of the memory block to be allocated.


## -remarks




<a href="https://msdn.microsoft.com/library/Ee419206(v=VS.85).aspx">XAPOFree</a> and <b>XAPOAlloc</b> are memory allocation macros that allow one module to allocate memory and another to free it, by guaranteeing that the same heap manager is used regardless of differences between the build environments of the two modules.

<table>
<tr>
<th>Xbox 360</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/Ee419206(v=VS.85).aspx">XAPOFree</a> and <b>XAPOAlloc</b> resolve to <b>XMemAlloc</b> and <b>XMemFree</b> on Xbox 360.</td>
</tr>
</table>
 

<table>
<tr>
<th>Windows</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/Ee419206(v=VS.85).aspx">XAPOFree</a> and <b>XAPOAlloc</b> resolve to <b>CoTaskMemAlloc</b> and <b>CoTaskMemFree</b>.</td>
</tr>
</table>
 

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/C39FBD61-16A1-4043-A5C2-0872F734F5FD">Macros</a>
 

 


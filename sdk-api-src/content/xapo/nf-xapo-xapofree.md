---
UID: NF:xapo.XAPOFree
title: XAPOFree macro
author: windows-sdk-content
description: Macro used to free memory allocated with the XAPOAlloc macro.
old-location: xaudio2\xapofree.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xapo.XAPOFree(void)
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: XAPOFree, XAPOFree macro [XAudio2 Audio Mixing APIs], xapo/XAPOFree, xaudio2.xapofree
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
 - XAPOFree
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# XAPOFree macro


## -description


Macro used to free memory allocated with the <a href="https://msdn.microsoft.com/en-us/library/Ee419205(v=VS.85).aspx">XAPOAlloc</a> macro. 


## -parameters




### -param p

Pointer to the memory block to be freed.


## -remarks



<b>XAPOFree</b> and <a href="https://msdn.microsoft.com/en-us/library/Ee419205(v=VS.85).aspx">XAPOAlloc</a> are memory allocation macros that allow one module to allocate memory and another to free it, by guaranteeing that the same heap manager is used regardless of differences between the build environments of the two modules.

<table>
<tr>
<th>Xbox 360</th>
</tr>
<tr>
<td><b>XAPOFree</b> and <a href="https://msdn.microsoft.com/en-us/library/Ee419205(v=VS.85).aspx">XAPOAlloc</a> resolve to <b>XMemAlloc</b> and <b>XMemFree</b> on Xbox 360.</td>
</tr>
</table>
 

<table>
<tr>
<th>Windows</th>
</tr>
<tr>
<td><b>XAPOFree</b> and <a href="https://msdn.microsoft.com/en-us/library/Ee419205(v=VS.85).aspx">XAPOAlloc</a> resolve to <b>CoTaskMemAlloc</b> and <b>CoTaskMemFree</b>.</td>
</tr>
</table>
 

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/C39FBD61-16A1-4043-A5C2-0872F734F5FD">Macros</a>
 

 


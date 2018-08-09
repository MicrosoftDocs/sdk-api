---
UID: NF:vfw.AVIStreamNearestKeyFrame
title: AVIStreamNearestKeyFrame macro
author: windows-sdk-content
description: The AVIStreamNearestKeyFrame macro locates the key frame at or preceding a specified position in a stream.
old-location: multimedia\avistreamnearestkeyframe.htm
old-project: Multimedia
ms.assetid: 90d0e0a8-dc5b-4f7e-868e-03f40f037437
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AVIStreamNearestKeyFrame, AVIStreamNearestKeyFrame macro [Windows Multimedia], _win32_AVIStreamNearestKeyFrame, multimedia.avistreamnearestkeyframe, vfw/AVIStreamNearestKeyFrame
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - AVIStreamNearestKeyFrame
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# AVIStreamNearestKeyFrame macro


## -description



The <b>AVIStreamNearestKeyFrame</b> macro locates the key frame at or preceding a specified position in a stream.




## -parameters




### -param pavi

Handle to an open stream. 


### -param l

Starting position to search in the stream. 


## -remarks



The <b>AVIStreamNearestKeyFrame</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define AVIStreamNearestKeyFrame(pavi, lPos) \ 
    AVIStreamFindSample(pavi, lPos , FIND_PREV | FIND_KEY) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 


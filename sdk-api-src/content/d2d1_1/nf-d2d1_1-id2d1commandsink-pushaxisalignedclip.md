---
UID: NF:d2d1_1.ID2D1CommandSink.PushAxisAlignedClip
title: ID2D1CommandSink::PushAxisAlignedClip
author: windows-sdk-content
description: Pushes a clipping rectangle onto the clip and layer stack.
old-location: direct2d\id2d1commandsink_pushaxisalignedclip.htm
tech.root: Direct2D
ms.assetid: 09e20780-2ebd-417e-9953-421f49dba4dd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID2D1CommandSink interface [Direct2D],PushAxisAlignedClip method, ID2D1CommandSink.PushAxisAlignedClip, ID2D1CommandSink::PushAxisAlignedClip, PushAxisAlignedClip, PushAxisAlignedClip method [Direct2D], PushAxisAlignedClip method [Direct2D],ID2D1CommandSink interface, d2d1_1/ID2D1CommandSink::PushAxisAlignedClip, direct2d.id2d1commandsink_pushaxisalignedclip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1CommandSink.PushAxisAlignedClip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1_1.h
: 
- ID2D1CommandSink.PushAxisAlignedClip
: 
---

# ID2D1CommandSink::PushAxisAlignedClip


## -description


Pushes a clipping rectangle onto the clip and layer stack.


## -parameters




### -param clipRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The rectangle that defines the clip.


### -param antialiasMode

Type: <b><a href="https://msdn.microsoft.com/3ca12155-6dd0-41bb-8778-3387422c4ffe">D2D1_ANTIALIAS_MODE</a></b>

The antialias mode for the clip.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





## -remarks



If the current world transform is not preserving the axis, <i>clipRectangle</i> is transformed and the bounds of the transformed rectangle are used instead.




## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/8b777425-07b1-4494-889a-0c947fb61315">ID2D1RenderTarget::PushAxisAlignedClip</a>
 

 


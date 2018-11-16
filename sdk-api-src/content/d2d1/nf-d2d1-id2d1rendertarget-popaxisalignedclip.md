---
UID: NF:d2d1.ID2D1RenderTarget.PopAxisAlignedClip
title: ID2D1RenderTarget::PopAxisAlignedClip
author: windows-sdk-content
description: Removes the last axis-aligned clip from the render target. After this method is called, the clip is no longer applied to subsequent drawing operations.
old-location: direct2d\ID2D1RenderTarget_PopAxisAlignedClip.htm
tech.root: Direct2D
ms.assetid: 0f0a2826-2356-4ced-a372-5bb59dd394ee
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],PopAxisAlignedClip method, ID2D1RenderTarget.PopAxisAlignedClip, ID2D1RenderTarget::PopAxisAlignedClip, PopAxisAlignedClip, PopAxisAlignedClip method [Direct2D], PopAxisAlignedClip method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::PopAxisAlignedClip, direct2d.ID2D1RenderTarget_PopAxisAlignedClip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
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
 - ID2D1RenderTarget.PopAxisAlignedClip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1.h
: 
- ID2D1RenderTarget.PopAxisAlignedClip
: 
---

# ID2D1RenderTarget::PopAxisAlignedClip


## -description


Removes the last axis-aligned clip from the render target. After this method is called, the clip is no longer applied to subsequent drawing operations.


## -parameters






## -returns



This method does not return a value.




## -remarks



A <a href="https://msdn.microsoft.com/db2e975e-e5c5-4c57-8071-ec042b9a6fb9">PushAxisAlignedClip</a>/<b>PopAxisAlignedClip</b> pair can occur around or within a <a href="https://msdn.microsoft.com/0fc7ac38-ff74-4f3b-9aa2-025a99e6b013">PushLayer</a>/<a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a> pair, but may not overlap. For example, a <b>PushAxisAlignedClip</b>, <b>PushLayer</b>, <b>PopLayer</b>, <b>PopAxisAlignedClip</b>  sequence is valid, but a <b>PushAxisAlignedClip</b>, <b>PushLayer</b>, <b>PopAxisAlignedClip</b>, <b>PopLayer</b> sequence is not. 

<b>PopAxisAlignedClip</b> must be called once for every call to <a href="https://msdn.microsoft.com/db2e975e-e5c5-4c57-8071-ec042b9a6fb9">PushAxisAlignedClip</a>.

For an example, see <a href="https://msdn.microsoft.com/4196653a-9177-4a41-9db9-4738a41313aa">How to Clip with an Axis-Aligned Clip Rectangle</a>.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>PopAxisAlignedClip</b>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 


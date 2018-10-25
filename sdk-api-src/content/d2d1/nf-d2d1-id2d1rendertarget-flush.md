---
UID: NF:d2d1.ID2D1RenderTarget.Flush
title: ID2D1RenderTarget::Flush
author: windows-sdk-content
description: Executes all pending drawing commands.
old-location: direct2d\ID2D1RenderTarget_Flush.htm
tech.root: direct2d
ms.assetid: 3ad9c966-85f5-4ddb-a8c1-aefcba533509
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: Flush, Flush method [Direct2D], Flush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],Flush method, ID2D1RenderTarget.Flush, ID2D1RenderTarget::Flush, d2d1/ID2D1RenderTarget::Flush, direct2d.ID2D1RenderTarget_Flush
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
 - ID2D1RenderTarget.Flush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::Flush


## -description


Executes all pending drawing commands.


## -parameters




### -param tag1 [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4f363295-f140-4149-ba78-3abbc56eebe8">D2D1_TAG</a>*</b>

When this method returns, contains the tag for drawing operations that caused errors or 0 if there were no errors. This parameter is passed uninitialized.


### -param tag2 [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4f363295-f140-4149-ba78-3abbc56eebe8">D2D1_TAG</a>*</b>

When this method returns, contains the tag for drawing operations that caused errors or 0 if there were no errors. This parameter is passed uninitialized.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code and sets <i>tag1</i> and <i>tag2</i> to the tags that were active when the error occurred. If no error occurred, this method sets the error tag state to be (0,0).




## -remarks



This command does not flush the Direct3D device context that is associated with the render target.

Calling this method resets the error state of the render target.




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 


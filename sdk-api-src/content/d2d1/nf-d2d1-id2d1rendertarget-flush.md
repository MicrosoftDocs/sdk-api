---
UID: NF:d2d1.ID2D1RenderTarget.Flush
title: ID2D1RenderTarget::Flush (d2d1.h)
description: Executes all pending drawing commands.
helpviewer_keywords: ["Flush","Flush method [Direct2D]","Flush method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","Flush method","ID2D1RenderTarget.Flush","ID2D1RenderTarget::Flush","d2d1/ID2D1RenderTarget::Flush","direct2d.ID2D1RenderTarget_Flush"]
old-location: direct2d\ID2D1RenderTarget_Flush.htm
tech.root: Direct2D
ms.assetid: 3ad9c966-85f5-4ddb-a8c1-aefcba533509
ms.date: 12/05/2018
ms.keywords: Flush, Flush method [Direct2D], Flush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],Flush method, ID2D1RenderTarget.Flush, ID2D1RenderTarget::Flush, d2d1/ID2D1RenderTarget::Flush, direct2d.ID2D1RenderTarget_Flush
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1RenderTarget::Flush
 - d2d1/ID2D1RenderTarget::Flush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget.Flush
---

# ID2D1RenderTarget::Flush


## -description

Executes all pending drawing commands.

## -parameters

### -param tag1 [out, optional]

Type: <b><a href="/windows/win32/Direct2D/d2d1-tag">D2D1_TAG</a>*</b>

When this method returns, contains the tag for drawing operations that caused errors or 0 if there were no errors. This parameter is passed uninitialized.

### -param tag2 [out, optional]

Type: <b><a href="/windows/win32/Direct2D/d2d1-tag">D2D1_TAG</a>*</b>

When this method returns, contains the tag for drawing operations that caused errors or 0 if there were no errors. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code and sets <i>tag1</i> and <i>tag2</i> to the tags that were active when the error occurred. If no error occurred, this method sets the error tag state to be (0,0).

## -remarks

This command does not flush the Direct3D device context that is associated with the render target.

Calling this method resets the error state of the render target.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>


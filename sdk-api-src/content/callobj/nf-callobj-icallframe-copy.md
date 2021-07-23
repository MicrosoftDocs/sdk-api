---
UID: NF:callobj.ICallFrame.Copy
title: ICallFrame::Copy (callobj.h)
description: Creates a copy of this call frame and all of its associated data.
helpviewer_keywords: ["Copy","Copy method [COM]","Copy method [COM]","ICallFrame interface","ICallFrame interface [COM]","Copy method","ICallFrame.Copy","ICallFrame::Copy","_com_icallframe_copy","callobj/ICallFrame::Copy","com.icallframe_copy"]
old-location: com\icallframe_copy.htm
tech.root: com
ms.assetid: bf2d2e55-d9d1-48d6-817c-382c739d1acd
ms.date: 12/05/2018
ms.keywords: Copy, Copy method [COM], Copy method [COM],ICallFrame interface, ICallFrame interface [COM],Copy method, ICallFrame.Copy, ICallFrame::Copy, _com_icallframe_copy, callobj/ICallFrame::Copy, com.icallframe_copy
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICallFrame::Copy
 - callobj/ICallFrame::Copy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallFrame.Copy
---

# ICallFrame::Copy


## -description

Creates a copy of this call frame and all of its associated data.
<div class="alert"><b>Warning</b>  The call frame does not clean up the copied data automatically. Therefore once the copy is returned then the user is responsible for calling <a href="/windows/desktop/api/callobj/nf-callobj-icallframe-free">Free</a> on the frame copy. This must be done to avoid a memory leak.</div><div> </div>

## -parameters

### -param copyControl [in]

Determines whether the copied call frame data can be shared with data in the parent frame by determining its lifetime dependency on the parent frame. For a list of values, see the <a href="/windows/win32/api/callobj/ne-callobj-callframe_copy">CALLFRAME_COPY</a> enumeration. If the CALLFRAME_COPY_NESTED flag is set, then the client will be responsible for using the copied call frame in a manner that its lifetime is nested in the lifetime of its parent frame making the data sharable. If the CALLFRAME_COPY_INDEPENDENT is set, then the lifetime of the copied frame will be independent of the parents.

### -param pWalker [in]

A pointer to an instance of the <a href="/windows/desktop/api/callobj/nn-callobj-icallframewalker">ICallFrameWalker</a> interface. The <a href="/windows/desktop/api/callobj/nf-callobj-icallframewalker-onwalkinterface">OnWalkInterface</a> method will be called for each interface pointer that is copied. If this parameter is not provided, then any interface pointer that is copied will be passed to <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a>.

### -param ppFrame [out]

A pointer to an <a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a> pointer to a copy of the call frame.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Copying a frame is like unmarshalling a marshaled frame. The call frame can only be copied if it has in-parameters. If the call frame is invoked, it cannot be copied. The copy method copies interface pointers as binary values and no referenced count adjustments are performed. But if this behavior is desired, then a pointer to <a href="/windows/desktop/api/callobj/nn-callobj-icallframewalker">ICallFrameWalker</a> can be used.

## -see-also

<a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>
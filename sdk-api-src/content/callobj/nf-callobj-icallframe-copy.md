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

# ICallFrame::Copy


## -description


Creates a copy of this call frame and all of its associated data.
<div class="alert"><b>Warning</b>  The call frame does not clean up the copied data automatically. Therefore once the copy is returned then the user is responsible for calling <a href="https://msdn.microsoft.com/97261d93-40cf-4a27-9bee-677600c04699">Free</a> on the frame copy. This must be done to avoid a memory leak.</div><div> </div>

## -parameters




### -param copyControl [in]

Determines whether the copied call frame data can be shared with data in the parent frame by determining its lifetime dependency on the parent frame. For a list of values, see the <a href="https://msdn.microsoft.com/06c926ab-8e82-4291-b1ea-f4bfcd734b16">CALLFRAME_COPY</a> enumeration. If the CALLFRAME_COPY_NESTED flag is set, then the client will be responsible for using the copied call frame in a manner that its lifetime is nested in the lifetime of its parent frame making the data sharable. If the CALLFRAME_COPY_INDEPENDENT is set, then the lifetime of the copied frame will be independent of the parents.


### -param pWalker [in]

A pointer to an instance of the <a href="https://msdn.microsoft.com/1eeb00a3-d3c5-46f0-95a8-f694f802894b">ICallFrameWalker</a> interface. The <a href="https://msdn.microsoft.com/e599536f-87a3-4f71-ac0e-21bdafafd029">OnWalkInterface</a> method will be called for each interface pointer that is copied. If this parameter is not provided, then any interface pointer that is copied will be passed to <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a>.


### -param ppFrame [out]

A pointer to an <a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a> pointer to a copy of the call frame.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Copying a frame is like unmarshalling a marshaled frame. The call frame can only be copied if it has in-parameters. If the call frame is invoked, it cannot be copied. The copy method copies interface pointers as binary values and no referenced count adjustments are performed. But if this behavior is desired, then a pointer to <a href="https://msdn.microsoft.com/1eeb00a3-d3c5-46f0-95a8-f694f802894b">ICallFrameWalker</a> can be used.




## -see-also




<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>
 

 


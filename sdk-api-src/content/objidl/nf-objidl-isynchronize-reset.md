---
UID: NF:objidl.ISynchronize.Reset
title: ISynchronize::Reset (objidl.h)
description: Sets the synchronization object to the nonsignaled state.
old-location: com\isynchronize_reset.htm
tech.root: com
ms.assetid: 33c56a33-9954-4612-ba0f-396ccdc48bf3
ms.date: 12/05/2018
ms.keywords: ISynchronize interface [COM],Reset method, ISynchronize.Reset, ISynchronize::Reset, Reset, Reset method [COM], Reset method [COM],ISynchronize interface, _com_isynchronize_reset, com.isynchronize_reset, objidlbase/ISynchronize::Reset
ms.topic: method
f1_keywords:
- objidl/ISynchronize.Reset
dev_langs:
- c++
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- objidlbase.h
api_name:
- ISynchronize.Reset
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISynchronize::Reset


## -description


Sets the synchronization object to the nonsignaled state.


## -parameters






## -returns



This method returns S_OK to indicate that the method completed successfully.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isynchronize-wait">ISynchronize::Wait</a> method implemented on a standard event object (CLSID_StdEvent) automatically calls <b>Reset</b> when the synchronization object has been signaled.

The implementation of <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isynchronize-wait">ISynchronize::Wait</a> on the manual reset event object (CLSID_ManualResetEvent) does not automatically call <b>Reset</b>. A server object usually calls <b>Reset</b> from a method that clients call after they detect that the synchronization object was signaled.

In general, it is the server's responsibility to call <b>Reset</b>. If, however, the client needs to begin with the synchronization object in an unsignaled state, the client should call <b>Reset</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-isynchronize">ISynchronize</a>
 

 


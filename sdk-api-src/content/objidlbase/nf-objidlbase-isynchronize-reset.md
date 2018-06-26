---
UID: NF:objidlbase.ISynchronize.Reset
title: ISynchronize::Reset
author: windows-sdk-content
description: Sets the synchronization object to the nonsignaled state.
old-location: com\isynchronize_reset.htm
old-project: com
ms.assetid: 33c56a33-9954-4612-ba0f-396ccdc48bf3
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ISynchronize interface [COM],Reset method, ISynchronize.Reset, ISynchronize::Reset, Reset, Reset method [COM], Reset method [COM],ISynchronize interface, _com_isynchronize_reset, com.isynchronize_reset, objidlbase/ISynchronize::Reset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidlbase.h
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
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ISynchronize.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISynchronize::Reset


## -description


Sets the synchronization object to the nonsignaled state.


## -parameters






## -returns



This method returns S_OK to indicate that the method completed successfully.




## -remarks



The <a href="https://msdn.microsoft.com/1abed0be-b4e3-41f4-af6c-e327ce934b59">ISynchronize::Wait</a> method implemented on a standard event object (CLSID_StdEvent) automatically calls <b>Reset</b> when the synchronization object has been signaled.

The implementation of <a href="https://msdn.microsoft.com/1abed0be-b4e3-41f4-af6c-e327ce934b59">ISynchronize::Wait</a> on the manual reset event object (CLSID_ManualResetEvent) does not automatically call <b>Reset</b>. A server object usually calls <b>Reset</b> from a method that clients call after they detect that the synchronization object was signaled.

In general, it is the server's responsibility to call <b>Reset</b>. If, however, the client needs to begin with the synchronization object in an unsignaled state, the client should call <b>Reset</b>.




## -see-also




<a href="https://msdn.microsoft.com/2c1e3d27-abb4-4bd0-ad9e-4dc9eda8e4b6">ISynchronize</a>
 

 


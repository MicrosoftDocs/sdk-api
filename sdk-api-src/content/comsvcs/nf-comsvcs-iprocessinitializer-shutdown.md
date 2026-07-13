---
UID: NF:comsvcs.IProcessInitializer.Shutdown
title: IProcessInitializer::Shutdown (comsvcs.h)
description: Called when Dllhost.exe shuts down.
helpviewer_keywords: ["IProcessInitializer interface [COM+]","Shutdown method","IProcessInitializer.Shutdown","IProcessInitializer::Shutdown","Shutdown","Shutdown method [COM+]","Shutdown method [COM+]","IProcessInitializer interface","_cos_IProcessInitializer_Shutdown","comsvcs/IProcessInitializer::Shutdown","cos.iprocessinitializer_shutdown"]
old-location: cos\iprocessinitializer_shutdown.htm
tech.root: cos
ms.assetid: e525ded0-971d-4711-b078-b2e6b28c313f
ms.date: 12/05/2018
ms.keywords: IProcessInitializer interface [COM+],Shutdown method, IProcessInitializer.Shutdown, IProcessInitializer::Shutdown, Shutdown, Shutdown method [COM+], Shutdown method [COM+],IProcessInitializer interface, _cos_IProcessInitializer_Shutdown, comsvcs/IProcessInitializer::Shutdown, cos.iprocessinitializer_shutdown
req.header: comsvcs.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IProcessInitializer::Shutdown
 - comsvcs/IProcessInitializer::Shutdown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IProcessInitializer.Shutdown
---

# IProcessInitializer::Shutdown


## -description

Called when Dllhost.exe shuts down.



## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

The Shutdown method is not called during a failfast or other catastrophic shutdown events.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iprocessinitializer">IProcessInitializer</a>

---
UID: NF:comsvcs.IProcessInitializer.Startup
title: IProcessInitializer::Startup (comsvcs.h)
description: Called when Dllhost.exe starts.
helpviewer_keywords: ["IProcessInitializer interface [COM+]","Startup method","IProcessInitializer.Startup","IProcessInitializer::Startup","Startup","Startup method [COM+]","Startup method [COM+]","IProcessInitializer interface","_cos_IProcessInitializer_Startup","comsvcs/IProcessInitializer::Startup","cos.iprocessinitializer_startup"]
old-location: cos\iprocessinitializer_startup.htm
tech.root: cos
ms.assetid: 0ba8844e-a1ef-4a1a-aef6-abd828ec59b0
ms.date: 12/05/2018
ms.keywords: IProcessInitializer interface [COM+],Startup method, IProcessInitializer.Startup, IProcessInitializer::Startup, Startup, Startup method [COM+], Startup method [COM+],IProcessInitializer interface, _cos_IProcessInitializer_Startup, comsvcs/IProcessInitializer::Startup, cos.iprocessinitializer_startup
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
 - IProcessInitializer::Startup
 - comsvcs/IProcessInitializer::Startup
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
 - IProcessInitializer.Startup
---

# IProcessInitializer::Startup


## -description

Called when Dllhost.exe starts.

## -parameters

### -param punkProcessControl [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the COM component starting up.

<b>Windows XP/2000:  </b>This parameter is always <b>NULL</b>.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

The <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface referenced by <i>punkProcessControl</i> must belong to a COM component that implements an <a href="/windows/desktop/api/objidl/nn-objidl-iprocessinitcontrol">IProcessInitControl</a> interface; this interface supports the single method <a href="/windows/desktop/api/objidl/nf-objidl-iprocessinitcontrol-resetinitializertimeout">ResetInitializerTimeout</a>. The initialization code in <b>Startup</b> can call the <b>ResetInitializerTimeout</b> method, with <i>dwSecondsRemaining</i> set equal to the number of seconds remaining before the startup of the component times out.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iprocessinitializer">IProcessInitializer</a>
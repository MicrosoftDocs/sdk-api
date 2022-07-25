---
UID: NF:objidl.IInitializeSpy.PreInitialize
title: IInitializeSpy::PreInitialize (objidl.h)
description: Performs initialization steps required before calling the CoInitializeEx function.
helpviewer_keywords: ["IInitializeSpy interface [COM]","PreInitialize method","IInitializeSpy.PreInitialize","IInitializeSpy::PreInitialize","PreInitialize","PreInitialize method [COM]","PreInitialize method [COM]","IInitializeSpy interface","_com_iinitializespy_preinitialize","com.iinitializespy_preinitialize","objidl/IInitializeSpy::PreInitialize"]
old-location: com\iinitializespy_preinitialize.htm
tech.root: com
ms.assetid: f5b345d1-ab37-401a-9cb4-b01ef7254fc8
ms.date: 12/05/2018
ms.keywords: IInitializeSpy interface [COM],PreInitialize method, IInitializeSpy.PreInitialize, IInitializeSpy::PreInitialize, PreInitialize, PreInitialize method [COM], PreInitialize method [COM],IInitializeSpy interface, _com_iinitializespy_preinitialize, com.iinitializespy_preinitialize, objidl/IInitializeSpy::PreInitialize
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInitializeSpy::PreInitialize
 - objidl/IInitializeSpy::PreInitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IInitializeSpy.PreInitialize
---

# IInitializeSpy::PreInitialize


## -description

Performs initialization steps required before calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> function.

## -parameters

### -param dwCoInit [in]

The apartment type passed to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>, specified as a member of the <a href="/windows/desktop/api/objbase/ne-objbase-coinit">COINIT</a> enumeration.

### -param dwCurThreadAptRefs [in]

The number of times <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> has been called on this thread.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iinitializespy">IInitializeSpy</a>
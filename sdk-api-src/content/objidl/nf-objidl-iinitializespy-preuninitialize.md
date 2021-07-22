---
UID: NF:objidl.IInitializeSpy.PreUninitialize
title: IInitializeSpy::PreUninitialize (objidl.h)
description: Performs cleanup steps required before calling the CoUninitialize function.
helpviewer_keywords: ["IInitializeSpy interface [COM]","PreUninitialize method","IInitializeSpy.PreUninitialize","IInitializeSpy::PreUninitialize","PreUninitialize","PreUninitialize method [COM]","PreUninitialize method [COM]","IInitializeSpy interface","_com_iinitializespy_preuninitialize","com.iinitializespy_preuninitialize","objidl/IInitializeSpy::PreUninitialize"]
old-location: com\iinitializespy_preuninitialize.htm
tech.root: com
ms.assetid: 22f9c663-0c6e-4413-a3a3-21cbb5ce62c9
ms.date: 12/05/2018
ms.keywords: IInitializeSpy interface [COM],PreUninitialize method, IInitializeSpy.PreUninitialize, IInitializeSpy::PreUninitialize, PreUninitialize, PreUninitialize method [COM], PreUninitialize method [COM],IInitializeSpy interface, _com_iinitializespy_preuninitialize, com.iinitializespy_preuninitialize, objidl/IInitializeSpy::PreUninitialize
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
 - IInitializeSpy::PreUninitialize
 - objidl/IInitializeSpy::PreUninitialize
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
 - IInitializeSpy.PreUninitialize
---

# IInitializeSpy::PreUninitialize


## -description

Performs cleanup steps required before calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> function.

## -parameters

### -param dwCurThreadAptRefs [in]

The number of times <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> has been called on this thread.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iinitializespy">IInitializeSpy</a>
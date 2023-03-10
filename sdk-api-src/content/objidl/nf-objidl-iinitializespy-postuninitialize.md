---
UID: NF:objidl.IInitializeSpy.PostUninitialize
title: IInitializeSpy::PostUninitialize (objidl.h)
description: Performs cleanup steps required after calling the CoUninitialize function.
helpviewer_keywords: ["IInitializeSpy interface [COM]","PostUninitialize method","IInitializeSpy.PostUninitialize","IInitializeSpy::PostUninitialize","PostUninitialize","PostUninitialize method [COM]","PostUninitialize method [COM]","IInitializeSpy interface","_com_iinitializespy_postuninitialize","com.iinitializespy_postuninitialize","objidl/IInitializeSpy::PostUninitialize"]
old-location: com\iinitializespy_postuninitialize.htm
tech.root: com
ms.assetid: f91a1a4a-4d0b-491e-a7c6-01596b5b9712
ms.date: 12/05/2018
ms.keywords: IInitializeSpy interface [COM],PostUninitialize method, IInitializeSpy.PostUninitialize, IInitializeSpy::PostUninitialize, PostUninitialize, PostUninitialize method [COM], PostUninitialize method [COM],IInitializeSpy interface, _com_iinitializespy_postuninitialize, com.iinitializespy_postuninitialize, objidl/IInitializeSpy::PostUninitialize
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
 - IInitializeSpy::PostUninitialize
 - objidl/IInitializeSpy::PostUninitialize
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
 - IInitializeSpy.PostUninitialize
---

# IInitializeSpy::PostUninitialize


## -description

Performs cleanup steps required after calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> function.

## -parameters

### -param dwNewThreadAptRefs [in]

The number of calls to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> remaining on this thread.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iinitializespy">IInitializeSpy</a>
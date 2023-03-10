---
UID: NN:objidl.IMallocSpy
title: IMallocSpy (objidl.h)
description: Enables application developers to monitor (spy on) memory allocation, detect memory leaks, and simulate memory failure in calls to IMalloc methods.
helpviewer_keywords: ["IMallocSpy","IMallocSpy interface [COM]","IMallocSpy interface [COM]","described","_com_imallocspy","com.imallocspy","objidl/IMallocSpy"]
old-location: com\imallocspy.htm
tech.root: com
ms.assetid: 8ba500f7-c070-4788-b7fe-58b6a4e6a94c
ms.date: 12/05/2018
ms.keywords: IMallocSpy, IMallocSpy interface [COM], IMallocSpy interface [COM],described, _com_imallocspy, com.imallocspy, objidl/IMallocSpy
req.header: objidl.h
req.include-header: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMallocSpy
 - objidl/IMallocSpy
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
 - IMallocSpy
---

# IMallocSpy interface


## -description

Enables application developers to monitor (spy on) memory allocation, detect memory leaks, and simulate memory failure in calls to <a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> methods.

## -inheritance

The <b>IMallocSpy</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMallocSpy</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc">CoGetMalloc</a>



<a href="/windows/desktop/api/objbase/nf-objbase-coregistermallocspy">CoRegisterMallocSpy</a>



<a href="/windows/desktop/api/objbase/nf-objbase-corevokemallocspy">CoRevokeMallocSpy</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a>

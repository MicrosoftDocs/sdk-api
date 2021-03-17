---
UID: NF:objidl.IInitializeSpy.PostInitialize
title: IInitializeSpy::PostInitialize (objidl.h)
description: Performs initialization steps required after calling the CoInitializeEx function.
helpviewer_keywords: ["IInitializeSpy interface [COM]","PostInitialize method","IInitializeSpy.PostInitialize","IInitializeSpy::PostInitialize","PostInitialize","PostInitialize method [COM]","PostInitialize method [COM]","IInitializeSpy interface","_com_iinitializespy_postinitialize","com.iinitializespy_postinitialize","objidl/IInitializeSpy::PostInitialize"]
old-location: com\iinitializespy_postinitialize.htm
tech.root: com
ms.assetid: bdef4089-93e6-4845-8dcc-1150d7a0d033
ms.date: 12/05/2018
ms.keywords: IInitializeSpy interface [COM],PostInitialize method, IInitializeSpy.PostInitialize, IInitializeSpy::PostInitialize, PostInitialize, PostInitialize method [COM], PostInitialize method [COM],IInitializeSpy interface, _com_iinitializespy_postinitialize, com.iinitializespy_postinitialize, objidl/IInitializeSpy::PostInitialize
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
 - IInitializeSpy::PostInitialize
 - objidl/IInitializeSpy::PostInitialize
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
 - IInitializeSpy.PostInitialize
---

# IInitializeSpy::PostInitialize


## -description

Performs initialization steps required after calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> function.

## -parameters

### -param hrCoInit [in]

The value returned by <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>.

### -param dwCoInit [in]

The apartment type passed to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>, specified as a member of the <a href="/windows/desktop/api/objbase/ne-objbase-coinit">COINIT</a> enumeration.

### -param dwNewThreadAptRefs [in]

The number of times <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> has been called on this thread.

## -returns

This method returns the value that it intends the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> call to return to its caller. For more information, see the Remarks section.

## -remarks

The return value from <b>PostInitialize</b> is intended to be the returned <b>HRESULT</b> from the call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>. This is always the case for a single active registration on this thread.

For cases where there are multiple registrations active on this thread, the returned <b>HRESULT</b> is arrived at by chaining of the various <b>PostInitialize</b> methods as follows: The COM determined <b>HRESULT</b> will be passed as the <i>hrCoInit</i> parameter to the first <b>PostInitialize</b> method called. The <b>HRESULT</b> from that <b>PostInitialize</b> call will be passed as the <i>hrCoInit</i> parameter to the next <b>PostInitialize</b> call. This chaining continues leading to the <b>HRESULT</b> from the last <b>PostInitialize</b> call being returned as the <b>HRESULT</b> from the call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iinitializespy">IInitializeSpy</a>
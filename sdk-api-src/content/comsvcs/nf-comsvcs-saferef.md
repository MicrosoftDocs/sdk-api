---
UID: NF:comsvcs.SafeRef
title: SafeRef function (comsvcs.h)
description: SafeRef function
helpviewer_keywords: ["SafeRef","SafeRef function [COM+]","_cos_SafeRef","comsvcs/SafeRef","cos.saferef"]
old-location: cos\saferef.htm
tech.root: cos
ms.assetid: 14d75a5e-33e8-4b35-9813-3632454b89b6
ms.date: 12/05/2018
ms.keywords: SafeRef, SafeRef function [COM+], _cos_SafeRef, comsvcs/SafeRef, cos.saferef
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
req.lib: ComSvcs.lib
req.dll: ComSvcs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SafeRef
 - comsvcs/SafeRef
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComSvcs.dll
api_name:
 - SafeRef
---

# SafeRef function


## -description

<p class="CCE_Message">[Do not use SafeRef in COM+. This function was used by objects in MTS to obtain a reference to itself. With COM+, this is no longer necessary.]

## -parameters

### -param rid [in]

A reference to the IID of the interface that the current object wants to pass to another object or client.

### -param pUnk [in]

A reference to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the current object.

## -returns

If the function succeeds, the return value is a pointer to the specified interface that can be passed outside the current object's context. Otherwise, the return value is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/cossdk/com--contexts-and-threading-models">COM+ Contexts and Threading Models</a>



<a href="/previous-versions/windows/desktop/legacy/ms679240(v=vs.85)">IMTxAS::SafeRef</a>
---
UID: NF:comsvcs.GetObjectContext
title: GetObjectContext macro (comsvcs.h)
description: Retrieves a reference to the context that is associated with the current COM+ object.
helpviewer_keywords: ["GetObjectContext","GetObjectContext function [COM+]","_cos_GetObjectContext","comsvcs/GetObjectContext","cos.getobjectcontext"]
old-location: cos\getobjectcontext.htm
tech.root: cos
ms.assetid: e93406df-e61c-4ee5-9cd4-828aab2c05b6
ms.date: 12/05/2018
ms.keywords: GetObjectContext, GetObjectContext function [COM+], _cos_GetObjectContext, comsvcs/GetObjectContext, cos.getobjectcontext
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
 - GetObjectContext
 - comsvcs/GetObjectContext
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
 - GetObjectContext
---

# GetObjectContext macro


## -description

Retrieves a reference to the context that is associated with the current COM+ object.

For similar functionality, see <a href="/previous-versions/windows/desktop/legacy/ms683405(v=vs.85)">IMTxAS::GetObjectContext</a>.

## -parameters

### -param ppIOC [out]

A reference to <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a> on the object's context. If the object's component has not been imported into an MTS package or if the <b>GetObjectContext</b> function is called from a constructor or an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> method, this parameter is set to a <b>NULL</b> pointer.

## -remarks

An object's context is not accessible from an object's constructor or from any <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> method.

An object should never attempt to pass its <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a> reference to another object. If you pass an <b>IObjectContext</b> reference to another object, it is no longer a valid reference.

When an object obtains a reference to its <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>, it must release the <b>IObjectContext</b> object when it is finished with it.

## -see-also

<a href="/windows/desktop/cossdk/com--contexts-and-threading-models">COM+ Contexts and Threading Models</a>



<a href="/previous-versions/windows/desktop/legacy/ms683405(v=vs.85)">IMTxAS::GetObjectContext</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>
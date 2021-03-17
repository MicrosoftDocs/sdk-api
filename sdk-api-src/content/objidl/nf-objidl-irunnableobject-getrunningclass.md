---
UID: NF:objidl.IRunnableObject.GetRunningClass
title: IRunnableObject::GetRunningClass (objidl.h)
description: Retrieves the CLSID of a running object.
helpviewer_keywords: ["GetRunningClass","GetRunningClass method [COM]","GetRunningClass method [COM]","IRunnableObject interface","IRunnableObject interface [COM]","GetRunningClass method","IRunnableObject.GetRunningClass","IRunnableObject::GetRunningClass","_com_irunnableobject_getrunningclass","com.irunnableobject_getrunningclass","objidl/IRunnableObject::GetRunningClass"]
old-location: com\irunnableobject_getrunningclass.htm
tech.root: com
ms.assetid: dfe80741-ceda-44cd-8506-1807bb664ad0
ms.date: 12/05/2018
ms.keywords: GetRunningClass, GetRunningClass method [COM], GetRunningClass method [COM],IRunnableObject interface, IRunnableObject interface [COM],GetRunningClass method, IRunnableObject.GetRunningClass, IRunnableObject::GetRunningClass, _com_irunnableobject_getrunningclass, com.irunnableobject_getrunningclass, objidl/IRunnableObject::GetRunningClass
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
 - IRunnableObject::GetRunningClass
 - objidl/IRunnableObject::GetRunningClass
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
 - IRunnableObject.GetRunningClass
---

# IRunnableObject::GetRunningClass


## -description

Retrieves the CLSID of a running object.

## -parameters

### -param lpClsid [out]

A pointer to the object's class identifier.

## -returns

This method can return the standard return values E_INVALIDARG, E_UNEXPECTED, and S_OK.

## -remarks

If an embedded document was created by an application that is not available on the user's computer, the document, by a call to <a href="/windows/desktop/api/objbase/nf-objbase-cotreatasclass">CoTreatAsClass</a>, may be able to display itself for editing by emulating a class that is supported on the user's machine. In this case, the CLSID returned by a call to <b>IRunnableObject::GetRunningClass</b> will be that of the class being emulated, rather than the document's native class.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irunnableobject">IRunnableObject</a>
---
UID: NF:ocidl.IPersistPropertyBag.InitNew
tech.root: com
title: IPersistPropertyBag::InitNew
ms.date: 05/25/2021
targetos: Windows
description: Informs the object that it is being initialized as a newly created object.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ocidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - ocidl.h
api_name:
 - IPersistPropertyBag::InitNew
f1_keywords:
 - IPersistPropertyBag::InitNew
 - ocidl/IPersistPropertyBag::InitNew
dev_langs:
 - c++
---

## -description

Informs the object that it is being initialized as a newly created object.

## -returns

## -remarks

E_NOTIMPL should not be returned. Return S_OK, even if the object does not perform any function in this method.

## -see-also


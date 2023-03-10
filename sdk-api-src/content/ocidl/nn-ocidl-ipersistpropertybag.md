---
UID: NN:ocidl.IPersistPropertyBag
tech.root: com
title: IPersistPropertyBag
ms.date: 05/25/2021
targetos: Windows
description: Works with [IPropertyBag](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) and [IErrorlog](/windows/win32/api/oaidl/nn-oaidl-ierrorlog) to define an individual property-based persistence mechanism.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: ocidl.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - ocidl.h
api_name:
 - IPersistPropertyBag
f1_keywords:
 - IPersistPropertyBag
 - ocidl/IPersistPropertyBag
dev_langs:
 - c++
---

## -description

Works with [IPropertyBag](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) and [IErrorlog](/windows/win32/api/oaidl/nn-oaidl-ierrorlog) to define an individual property-based persistence mechanism.

## -remarks

**IPersistPropertyBag** provides an object with an IPropertyBag interface through which it can save and load individual properties. The object that implements **IPropertyBag** can then save those properties in various ways, such as name/value pairs in a text file. Errors encountered in the process (on either side) are recorded in an error log through IErrorlog. This error reporting mechanism works on a per-property basis instead of on all properties at once.

## -see-also


---
UID: NF:dinputd.IDirectInputJoyConfig8.AddRef
title: IDirectInputJoyConfig8::AddRef (dinputd.h)
description: The IDirectInputJoyConfig8::AddRef method increases the reference count of the DirectInputJoyConfig object by 1. This method is part of the IUnknown interface inherited by DirectInputJoyConfig.
helpviewer_keywords: ["AddRef","AddRef method [Human Input Devices]","AddRef method [Human Input Devices]","IDirectInputJoyConfig8 interface","IDirectInputJoyConfig8 interface [Human Input Devices]","AddRef method","IDirectInputJoyConfig8.AddRef","IDirectInputJoyConfig8::AddRef","di_ref_5b8306ac-22f0-48f9-af91-a83d6bd8b936.xml","dinputd/IDirectInputJoyConfig8::AddRef","hid.idirectinputjoyconfig8_addref"]
old-location: hid\idirectinputjoyconfig8_addref.htm
tech.root: hid
ms.assetid: 04e10558-367e-495c-aa1a-43344f803c8a
ms.date: 12/05/2018
ms.keywords: AddRef, AddRef method [Human Input Devices], AddRef method [Human Input Devices],IDirectInputJoyConfig8 interface, IDirectInputJoyConfig8 interface [Human Input Devices],AddRef method, IDirectInputJoyConfig8.AddRef, IDirectInputJoyConfig8::AddRef, di_ref_5b8306ac-22f0-48f9-af91-a83d6bd8b936.xml, dinputd/IDirectInputJoyConfig8::AddRef, hid.idirectinputjoyconfig8_addref
req.header: dinputd.h
req.include-header: Dinputd.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IDirectInputJoyConfig8::AddRef
 - dinputd/IDirectInputJoyConfig8::AddRef
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dinputd.h
api_name:
 - IDirectInputJoyConfig8.AddRef
---

# IDirectInputJoyConfig8::AddRef


## -description

The <b>IDirectInputJoyConfig8::AddRef</b> method increases the reference count of the DirectInputJoyConfig object by 1. This method is part of the <b>IUnknown</b> interface inherited by DirectInputJoyConfig.



## -returns

Returns the new reference count of the object.

## -remarks

When the DirectInputJoyConfig object is created, its reference count should be set to 1. Every time an application obtains an interface to the object or calls the <b>AddRef</b> method, the object's reference count is increased by 1. The application uses the <b>Release</b> method to decrease the reference count of the object by 1.


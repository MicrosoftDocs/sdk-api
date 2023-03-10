---
UID: NN:objidl.ILockBytes
title: ILockBytes (objidl.h)
description: The ILockBytes interface is implemented on a byte array object that is backed by some physical storage, such as a disk file, global memory, or a database.
helpviewer_keywords: ["ILockBytes","ILockBytes interface [Structured Storage]","ILockBytes interface [Structured Storage]","described","_stg_ilockbytes","objidl/ILockBytes","stg.ilockbytes"]
old-location: stg\ilockbytes.htm
tech.root: Stg
ms.assetid: bb2c5d0d-8dc8-4844-9a20-ef8e4def5731
ms.date: 12/05/2018
ms.keywords: ILockBytes, ILockBytes interface [Structured Storage], ILockBytes interface [Structured Storage],described, _stg_ilockbytes, objidl/ILockBytes, stg.ilockbytes
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILockBytes
 - objidl/ILockBytes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - ILockBytes
---

# ILockBytes interface


## -description

The 
<b>ILockBytes</b> interface is implemented on a byte array object that is backed by some physical storage, such as a disk file, global memory, or a database. It is used by a COM compound file storage object to give its root storage access to the physical device, while isolating the root storage from the details of accessing the physical storage.

## -inheritance

The <b>ILockBytes</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILockBytes</b> also has these types of members:


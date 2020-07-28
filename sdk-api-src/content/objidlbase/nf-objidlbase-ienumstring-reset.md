---
UID: NF:objidlbase.IEnumString.Reset
title: IEnumString::Reset (objidlbase.h)
description: Resets the enumeration sequence to the beginning.
helpviewer_keywords: ["IEnumString interface [COM]","Reset method","IEnumString.Reset","IEnumString::Reset","Reset","Reset method [COM]","Reset method [COM]","IEnumString interface","_com_ienumstring_reset","com.ienumstring_reset","objidlbase/IEnumString::Reset"]
old-location: com\ienumstring_reset.htm
tech.root: com
ms.assetid: 6f134738-b5ed-4f45-bf91-eeb28c8965c6
ms.date: 12/05/2018
ms.keywords: IEnumString interface [COM],Reset method, IEnumString.Reset, IEnumString::Reset, Reset, Reset method [COM], Reset method [COM],IEnumString interface, _com_ienumstring_reset, com.ienumstring_reset, objidlbase/IEnumString::Reset
f1_keywords:
- objidlbase/IEnumString.Reset
dev_langs:
- c++
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- objidlbase.h
api_name:
- IEnumString.Reset
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumString::Reset


## -description


Resets the enumeration sequence to the beginning.


## -parameters






## -returns



The return value is S_OK.




## -remarks



There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>
 

 


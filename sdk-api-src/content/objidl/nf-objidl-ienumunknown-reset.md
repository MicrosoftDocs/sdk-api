---
UID: NF:objidl.IEnumUnknown.Reset
title: IEnumUnknown::Reset (objidl.h)
description: Resets the enumeration sequence to the beginning.helpviewer_keywords: ["IEnumUnknown interface [COM]","Reset method","IEnumUnknown.Reset","IEnumUnknown::Reset","Reset","Reset method [COM]","Reset method [COM]","IEnumUnknown interface","_com_ienumunknown_reset","com.ienumunknown_reset","objidlbase/IEnumUnknown::Reset"]
old-location: com\ienumunknown_reset.htm
tech.root: com
ms.assetid: 54c60e75-1b23-4e89-af16-e551ed880a61
ms.date: 12/05/2018
ms.keywords: IEnumUnknown interface [COM],Reset method, IEnumUnknown.Reset, IEnumUnknown::Reset, Reset, Reset method [COM], Reset method [COM],IEnumUnknown interface, _com_ienumunknown_reset, com.ienumunknown_reset, objidlbase/IEnumUnknown::Reset
f1_keywords:
- objidl/IEnumUnknown.Reset
dev_langs:
- c++
req.header: objidl.h
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
- IEnumUnknown.Reset
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumUnknown::Reset


## -description


Resets the enumeration sequence to the beginning.


## -parameters






## -returns



The return value is S_OK.




## -remarks



There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a>
 

 


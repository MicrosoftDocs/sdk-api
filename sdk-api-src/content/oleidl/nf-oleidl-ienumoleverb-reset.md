---
UID: NF:oleidl.IEnumOLEVERB.Reset
title: IEnumOLEVERB::Reset (oleidl.h)
description: Resets the enumeration sequence to the beginning.
old-location: com\ienumoleverb_reset.htm
tech.root: com
ms.assetid: 612a364a-e7c2-4efd-b55c-1050891f5e22
ms.date: 12/05/2018
ms.keywords: IEnumOLEVERB interface [COM],Reset method, IEnumOLEVERB.Reset, IEnumOLEVERB::Reset, Reset, Reset method [COM], Reset method [COM],IEnumOLEVERB interface, _ole_ienumoleverb_reset, com.ienumoleverb_reset, oleidl/IEnumOLEVERB::Reset
f1_keywords:
- oleidl/IEnumOLEVERB.Reset
dev_langs:
- c++
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
- OleIdl.h
api_name:
- IEnumOLEVERB.Reset
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumOLEVERB::Reset


## -description


Resets the enumeration sequence to the beginning.


## -parameters






## -returns



This method returns S_OK on success.




## -remarks



There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ienumoleverb">IEnumOLEVERB</a>
 

 


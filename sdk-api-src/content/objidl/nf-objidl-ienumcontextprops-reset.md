---
UID: NF:objidl.IEnumContextProps.Reset
title: IEnumContextProps::Reset (objidl.h)
description: Resets the enumeration sequence to the beginning.helpviewer_keywords: ["IEnumContextProps interface [COM]","Reset method","IEnumContextProps.Reset","IEnumContextProps::Reset","Reset","Reset method [COM]","Reset method [COM]","IEnumContextProps interface","_com_ienumcontextprops_reset","com.ienumcontextprops_reset","objidlbase/IEnumContextProps::Reset"]
old-location: com\ienumcontextprops_reset.htm
tech.root: com
ms.assetid: de6a45d2-f0f7-4233-92d2-8e59d4685557
ms.date: 12/05/2018
ms.keywords: IEnumContextProps interface [COM],Reset method, IEnumContextProps.Reset, IEnumContextProps::Reset, Reset, Reset method [COM], Reset method [COM],IEnumContextProps interface, _com_ienumcontextprops_reset, com.ienumcontextprops_reset, objidlbase/IEnumContextProps::Reset
f1_keywords:
- objidl/IEnumContextProps.Reset
dev_langs:
- c++
req.header: objidl.h
req.include-header: ObjIdl.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- objidlbase.h
api_name:
- IEnumContextProps.Reset
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumContextProps::Reset


## -description


Resets the enumeration sequence to the beginning.


## -parameters






## -returns



The return value is S_OK.




## -remarks



There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumcontextprops">IEnumContextProps</a>
 

 


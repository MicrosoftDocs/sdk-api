---
UID: NF:objidl.IEnumMoniker.Reset
title: IEnumMoniker::Reset (objidl.h)
author: windows-sdk-content
description: Resets the enumeration sequence to the beginning.
old-location: com\ienummoniker_reset.htm
tech.root: com
ms.assetid: 0b7c74b4-cbcb-44cc-8bea-feb55abb5643
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumMoniker interface [COM],Reset method, IEnumMoniker.Reset, IEnumMoniker::Reset, Reset, Reset method [COM], Reset method [COM],IEnumMoniker interface, _ole_ienummoniker_reset, com.ienummoniker_reset, objidl/IEnumMoniker::Reset
ms.topic: method
f1_keywords: ["objidl/IEnumMoniker.Reset"]
req.header: objidl.h
req.include-header: 
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
 - ObjIdl.h
api_name:
 - IEnumMoniker.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumMoniker::Reset


## -description


Resets the enumeration sequence to the beginning.


## -parameters






## -returns



This method returns S_OK on success.




## -remarks



There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienummoniker">IEnumMoniker</a>
 

 


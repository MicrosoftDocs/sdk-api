---
UID: NF:objidl.IEnumContextProps.Reset
title: IEnumContextProps::Reset method
author: windows-driver-content
description: Resets the enumeration sequence to the beginning.
old-location: com\ienumcontextprops_reset.htm
old-project: com
ms.assetid: de6a45d2-f0f7-4233-92d2-8e59d4685557
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IEnumContextProps, IEnumContextProps interface [COM], Reset method, IEnumContextProps::Reset, Reset method [COM], Reset method [COM], IEnumContextProps interface, Reset,IEnumContextProps.Reset, _com_ienumcontextprops_reset, com.ienumcontextprops_reset, objidlbase/IEnumContextProps::Reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objidlbase.h
api_name:
-	IEnumContextProps.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IEnumContextProps::Reset method


## -description


Resets the enumeration sequence to the beginning.


## -parameters






## -returns



The return value is S_OK.




## -remarks



There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.




## -see-also




<a href="https://msdn.microsoft.com/64591e45-5478-4360-8c1f-08b09b5aef8e">IEnumContextProps</a>
 

 


---
UID: NF:objidlbase.IEnumUnknown.Reset
title: IEnumUnknown::Reset method
author: windows-driver-content
description: Resets the enumeration sequence to the beginning.
old-location: com\ienumunknown_reset.htm
old-project: com
ms.assetid: 54c60e75-1b23-4e89-af16-e551ed880a61
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IEnumUnknown, IEnumUnknown interface [COM], Reset method, IEnumUnknown::Reset, Reset method [COM], Reset method [COM], IEnumUnknown interface, Reset,IEnumUnknown.Reset, _com_ienumunknown_reset, com.ienumunknown_reset, objidlbase/IEnumUnknown::Reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
-	IEnumUnknown.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IEnumUnknown::Reset method


## -description


Resets the enumeration sequence to the beginning.


## -parameters






## -returns



The return value is S_OK.




## -remarks



There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.




## -see-also




<a href="https://msdn.microsoft.com/5aaed96f-39c1-4201-80d0-a2a8a177b65e">IEnumUnknown</a>
 

 


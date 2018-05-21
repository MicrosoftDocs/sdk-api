---
UID: NF:objidl.IEnumString.Reset
title: IEnumString::Reset
author: windows-driver-content
description: Resets the enumeration sequence to the beginning.
old-location: com\ienumstring_reset.htm
old-project: com
ms.assetid: 6f134738-b5ed-4f45-bf91-eeb28c8965c6
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IEnumString interface [COM],Reset method, IEnumString.Reset, IEnumString::Reset, Reset, Reset method [COM], Reset method [COM],IEnumString interface, _com_ienumstring_reset, com.ienumstring_reset, objidlbase/IEnumString::Reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
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
-	IEnumString.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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




<a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a>
 

 


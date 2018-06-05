---
UID: NF:oleidl.IEnumOLEVERB.Reset
title: IEnumOLEVERB::Reset
author: windows-sdk-content
description: Resets the enumeration sequence to the beginning.
old-location: com\ienumoleverb_reset.htm
old-project: com
ms.assetid: 612a364a-e7c2-4efd-b55c-1050891f5e22
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IEnumOLEVERB interface [COM],Reset method, IEnumOLEVERB.Reset, IEnumOLEVERB::Reset, Reset, Reset method [COM], Reset method [COM],IEnumOLEVERB interface, _ole_ienumoleverb_reset, com.ienumoleverb_reset, oleidl/IEnumOLEVERB::Reset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IEnumOLEVERB.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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




<a href="https://msdn.microsoft.com/fc9b3474-6f56-4274-af7d-72e0920c0457">IEnumOLEVERB</a>
 

 


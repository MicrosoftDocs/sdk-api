---
UID: NF:objidl.IEnumFORMATETC.Reset
title: IEnumFORMATETC::Reset
author: windows-sdk-content
description: Resets the enumeration sequence to the beginning.
old-location: com\ienumformatetc_reset.htm
old-project: com
ms.assetid: f079c166-c4a8-4827-a8c5-3c5e0cb13b77
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IEnumFORMATETC interface [COM],Reset method, IEnumFORMATETC.Reset, IEnumFORMATETC::Reset, Reset, Reset method [COM], Reset method [COM],IEnumFORMATETC interface, _ole_ienumformatetc_reset, com.ienumformatetc_reset, objidl/IEnumFORMATETC::Reset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
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
-	ObjIdl.h
api_name:
-	IEnumFORMATETC.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumFORMATETC::Reset


## -description


Resets the enumeration sequence to the beginning.


## -parameters






## -returns



This method returns S_OK on success.




## -remarks



There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.




## -see-also




<a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a>
 

 


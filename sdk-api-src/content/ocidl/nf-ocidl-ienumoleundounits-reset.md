---
UID: NF:ocidl.IEnumOleUndoUnits.Reset
title: IEnumOleUndoUnits::Reset
author: windows-sdk-content
description: Resets the enumeration sequence to the beginning.
old-location: com\ienumoleundounits_reset.htm
old-project: com
ms.assetid: 14336909-539c-41ac-a3a6-73be04fa72d1
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IEnumOleUndoUnits interface [COM],Reset method, IEnumOleUndoUnits.Reset, IEnumOleUndoUnits::Reset, Reset, Reset method [COM], Reset method [COM],IEnumOleUndoUnits interface, _ole_ienumoleundounits_reset, com.ienumoleundounits_reset, ocidl/IEnumOleUndoUnits::Reset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IEnumOleUndoUnits.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumOleUndoUnits::Reset


## -description


Resets the enumeration sequence to the beginning.


## -parameters






## -returns



This method returns S_OK on success. 




## -remarks



There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.




## -see-also




<a href="https://msdn.microsoft.com/f43cbd9d-d91b-4230-816f-693dec7056a4">IEnumOleUndoUnits</a>
 

 


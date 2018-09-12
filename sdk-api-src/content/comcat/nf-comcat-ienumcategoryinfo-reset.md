---
UID: NF:comcat.IEnumCATEGORYINFO.Reset
title: IEnumCATEGORYINFO::Reset
author: windows-sdk-content
description: Resets the enumeration sequence to the beginning.
old-location: com\ienumcategoryinfo_reset.htm
tech.root: com
ms.assetid: 55b9197e-4138-4cd5-9d06-4f31f1f5781a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IEnumCATEGORYINFO interface [COM],Reset method, IEnumCATEGORYINFO.Reset, IEnumCATEGORYINFO::Reset, Reset, Reset method [COM], Reset method [COM],IEnumCATEGORYINFO interface, _com_ienumcategoryinfo_reset, com.ienumcategoryinfo_reset, comcat/IEnumCATEGORYINFO::Reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comcat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Comcat.idl
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
 - ComCat.h
api_name:
 - IEnumCATEGORYINFO.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCATEGORYINFO::Reset


## -description


Resets the enumeration sequence to the beginning.


## -parameters






## -returns



The return value is S_OK.




## -remarks



There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.




## -see-also




<a href="https://msdn.microsoft.com/87469ace-ae34-40e5-aab6-f26a4bc50b54">IEnumCATEGORYINFO</a>
 

 


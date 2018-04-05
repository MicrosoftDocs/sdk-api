---
UID: NF:ocidl.IEnumConnections.Reset
title: IEnumConnections::Reset method
author: windows-driver-content
description: Resets the enumeration sequence to the beginning.
old-location: com\ienumconnections_reset.htm
old-project: com
ms.assetid: 444c9398-199f-4d87-9b1e-075d5af0b649
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IEnumConnections, IEnumConnections interface [COM], Reset method, IEnumConnections::Reset, Reset method [COM], Reset method [COM], IEnumConnections interface, Reset,IEnumConnections.Reset, _com_ienumconnections_reset, com.ienumconnections_reset, ocidl/IEnumConnections::Reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
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
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ocidl.h
api_name:
-	IEnumConnections.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IEnumConnections::Reset method


## -description


Resets the enumeration sequence to the beginning.


## -parameters






## -returns



The return value is S_OK.




## -remarks



There is no guarantee that the same set of objects will be enumerated after the reset operation has completed. A static collection is reset to the beginning, but it can be too expensive for some collections, such as files in a directory, to guarantee this condition.




## -see-also




<a href="https://msdn.microsoft.com/464966c1-e4e9-4b58-9e41-48de408f572f">IEnumConnections</a>
 

 


---
UID: NS:commctrl.tagLVINSERTGROUPSORTED
title: tagLVINSERTGROUPSORTED
author: windows-driver-content
description: Used to sort groups. It is used with LVM_INSERTGROUPSORTED.
old-location: controls\LVINSERTGROUPSORTED.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvinsertgroupsorted.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: "*PLVINSERTGROUPSORTED, LVINSERTGROUPSORTED, LVINSERTGROUPSORTED structure [Windows Controls], PLVINSERTGROUPSORTED, PLVINSERTGROUPSORTED structure pointer [Windows Controls], commctrl/LVINSERTGROUPSORTED, commctrl/PLVINSERTGROUPSORTED, controls.LVINSERTGROUPSORTED, controls.inet_LVINSERTGROUPSORTED, inet_LVINSERTGROUPSORTED, inet_LVINSERTGROUPSORTED_cpp, tagLVINSERTGROUPSORTED"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: LVINSERTGROUPSORTED, *PLVINSERTGROUPSORTED
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	LVINSERTGROUPSORTED
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagLVINSERTGROUPSORTED structure


## -description


Used to sort groups. It is used with <a href="https://msdn.microsoft.com/8ad1660b-8b64-4f02-ac1b-b7edeeea38ab">LVM_INSERTGROUPSORTED</a>.


## -struct-fields




### -field pfnGroupCompare

Type: <b>PFNLVGROUPCOMPARE</b>

Pointer to application-defined function <a href="https://msdn.microsoft.com/18e93f11-d215-4c16-b873-5c7b1e725886">LVGroupCompare</a> that is used to sort the groups.


### -field pvData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPVOID</a>*</b>

Data to sort; this is application-defined.


### -field lvGroup

Type: <b><a href="https://msdn.microsoft.com/512a8524-d5f9-47c0-a28e-47c3c1a713bf">LVGROUP</a></b>

Group to sort; this is application-defined.


## -see-also




<a href="https://msdn.microsoft.com/18e93f11-d215-4c16-b873-5c7b1e725886">LVGroupCompare</a>



<a href="https://msdn.microsoft.com/8ad1660b-8b64-4f02-ac1b-b7edeeea38ab">LVM_INSERTGROUPSORTED</a>



<b>Reference</b>
 

 


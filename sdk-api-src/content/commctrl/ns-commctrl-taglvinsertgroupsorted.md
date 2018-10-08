---
UID: NS:commctrl.tagLVINSERTGROUPSORTED
title: tagLVINSERTGROUPSORTED
author: windows-sdk-content
description: Used to sort groups. It is used with LVM_INSERTGROUPSORTED.
old-location: controls\LVINSERTGROUPSORTED.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvinsertgroupsorted.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PLVINSERTGROUPSORTED, LVINSERTGROUPSORTED, LVINSERTGROUPSORTED structure [Windows Controls], PLVINSERTGROUPSORTED, PLVINSERTGROUPSORTED structure pointer [Windows Controls], commctrl/LVINSERTGROUPSORTED, commctrl/PLVINSERTGROUPSORTED, controls.LVINSERTGROUPSORTED, controls.inet_LVINSERTGROUPSORTED, inet_LVINSERTGROUPSORTED, inet_LVINSERTGROUPSORTED_cpp, tagLVINSERTGROUPSORTED"
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - LVINSERTGROUPSORTED
product: Windows
targetos: Windows
req.typenames: LVINSERTGROUPSORTED, *PLVINSERTGROUPSORTED
req.redist: 
---

# tagLVINSERTGROUPSORTED structure


## -description


Used to sort groups. It is used with <a href="https://msdn.microsoft.com/en-us/library/Bb761105(v=VS.85).aspx">LVM_INSERTGROUPSORTED</a>.


## -struct-fields




### -field pfnGroupCompare

Type: <b>PFNLVGROUPCOMPARE</b>

Pointer to application-defined function <a href="https://msdn.microsoft.com/en-us/library/Bb775142(v=VS.85).aspx">LVGroupCompare</a> that is used to sort the groups.


### -field pvData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPVOID</a>*</b>

Data to sort; this is application-defined.


### -field lvGroup

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb774769(v=VS.85).aspx">LVGROUP</a></b>

Group to sort; this is application-defined.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775142(v=VS.85).aspx">LVGroupCompare</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761105(v=VS.85).aspx">LVM_INSERTGROUPSORTED</a>



<b>Reference</b>
 

 


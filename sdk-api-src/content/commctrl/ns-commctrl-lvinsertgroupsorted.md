---
UID: NS:commctrl.tagLVINSERTGROUPSORTED
title: LVINSERTGROUPSORTED (commctrl.h)
author: windows-sdk-content
description: Used to sort groups. It is used with LVM_INSERTGROUPSORTED.
old-location: controls\LVINSERTGROUPSORTED.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvinsertgroupsorted.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PLVINSERTGROUPSORTED, LVINSERTGROUPSORTED, LVINSERTGROUPSORTED structure [Windows Controls], PLVINSERTGROUPSORTED, PLVINSERTGROUPSORTED structure pointer [Windows Controls], commctrl/LVINSERTGROUPSORTED, commctrl/PLVINSERTGROUPSORTED, controls.LVINSERTGROUPSORTED, controls.inet_LVINSERTGROUPSORTED, inet_LVINSERTGROUPSORTED, inet_LVINSERTGROUPSORTED_cpp"
ms.topic: struct
f1_keywords: 
 - "commctrl/LVINSERTGROUPSORTED"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: LVINSERTGROUPSORTED, *PLVINSERTGROUPSORTED
req.redist: 
ms.custom: 19H1
---

# LVINSERTGROUPSORTED structure


## -description


Used to sort groups. It is used with <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-insertgroupsorted">LVM_INSERTGROUPSORTED</a>.


## -struct-fields




### -field pfnGroupCompare

Type: <b>PFNLVGROUPCOMPARE</b>

Pointer to application-defined function <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a> that is used to sort the groups.


### -field pvData

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPVOID</a>*</b>

Data to sort; this is application-defined.


### -field lvGroup

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-lvgroup">LVGROUP</a></b>

Group to sort; this is application-defined.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-insertgroupsorted">LVM_INSERTGROUPSORTED</a>



<b>Reference</b>
 

 


---
UID: NC:commctrl.PFNLVGROUPCOMPARE
title: PFNLVGROUPCOMPARE (commctrl.h)
author: windows-sdk-content
description: The LVGroupCompare function is an application-defined callback function used with the LVM_INSERTGROUPSORTED and LVM_SORTGROUPS messages.
old-location: controls\LVGroupCompare.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\callbackfunctions\lvgroupcompare.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: LVGroupCompare, PFNLVGROUPCOMPARE, PFNLVGROUPCOMPARE callback, PFNLVGROUPCOMPARE callback function [Windows Controls], _win32_LVGroupCompare, _win32_LVGroupCompare_cpp, commctrl/PFNLVGROUPCOMPARE, controls.LVGroupCompare, controls._win32_LVGroupCompare
ms.topic: callback
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
 - UserDefined
api_location:
 - Commctrl.h
api_name:
 - PFNLVGROUPCOMPARE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFNLVGROUPCOMPARE callback function


## -description


The <b>LVGroupCompare</b> function is an application-defined callback function used with the <a href="https://msdn.microsoft.com/en-us/library/Bb761105(v=VS.85).aspx">LVM_INSERTGROUPSORTED</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb761225(v=VS.85).aspx">LVM_SORTGROUPS</a> messages. It defines the ordering of the groups, based on the ID. The 
			<b>LVGROUPCOMPARE</b> type defines a pointer to this callback function. <b>LVGroupCompare</b> is a placeholder for the application-defined function name. 


## -parameters




### -param Arg1


### -param Arg2


### -param *








#### - Group1_ID [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The ID of the first group.


#### - Group2_ID [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The ID of the second group.


#### - pvData [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">VOID</a>*</b>

A pointer to the application-defined information. This comes from the message that was called; for <a href="https://msdn.microsoft.com/en-us/library/Bb761105(v=VS.85).aspx">LVM_INSERTGROUPSORTED</a> it is <a href="https://msdn.microsoft.com/en-us/library/Bb774756(v=VS.85).aspx">LVINSERTGROUPSORTED.pvData</a>, and for <a href="https://msdn.microsoft.com/en-us/library/Bb761225(v=VS.85).aspx">LVM_SORTGROUPS</a> it is the <i>plv</i> parameter.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Returns a negative value if the data for <i>Group1_ID</i> is less than the data for <i>Group2_ID</i>, a positive value if it is greater, or zero if it is the same.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774756(v=VS.85).aspx">LVINSERTGROUPSORTED</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761105(v=VS.85).aspx">LVM_INSERTGROUPSORTED</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761225(v=VS.85).aspx">LVM_SORTGROUPS</a>



<b>Reference</b>
 

 


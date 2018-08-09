---
UID: NC:winnt.PAPCFUNC
title: PAPCFUNC
author: windows-sdk-content
description: An application-defined completion routine. Specify this address when calling the QueueUserAPC function.
old-location: base\apcproc.htm
old-project: sync
ms.assetid: 8d52ad73-0172-4d1d-b625-39629e7f5823
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: APCProc, APCProc callback, APCProc callback function, PAPCFUNC, _win32_apcproc, base.apcproc, winnt/APCProc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: NUMBERFMTW, *LPNUMBERFMTW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winnt.h
api_name:
 - APCProc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PAPCFUNC callback function


## -description


An application-defined completion routine. Specify this address when calling the 
<a href="https://msdn.microsoft.com/5b141372-7c95-4eb2-987b-64fdf7d0783d">QueueUserAPC</a> function. The <b>PAPCFUNC</b> type defines a pointer to this callback function. 
<b>APCProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param Parameter








#### - dwParam [in]

The data passed to the function using the <i>dwData</i> parameter of the 
<a href="https://msdn.microsoft.com/5b141372-7c95-4eb2-987b-64fdf7d0783d">QueueUserAPC</a> function.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540625">Asynchronous Procedure Calls</a>



<a href="https://msdn.microsoft.com/5b141372-7c95-4eb2-987b-64fdf7d0783d">QueueUserAPC</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 


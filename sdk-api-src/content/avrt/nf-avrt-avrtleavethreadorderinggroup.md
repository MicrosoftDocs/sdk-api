---
UID: NF:avrt.AvRtLeaveThreadOrderingGroup
title: AvRtLeaveThreadOrderingGroup function (avrt.h)
author: windows-sdk-content
description: Enables client threads to leave a thread ordering group.
old-location: base\avrtleavethreadorderinggroup.htm
tech.root: ProcThread
ms.assetid: b618c312-0a43-4815-ad32-8820c658dc0b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AvRtLeaveThreadOrderingGroup, AvRtLeaveThreadOrderingGroup function, avrt/AvRtLeaveThreadOrderingGroup, base.avrtleavethreadorderinggroup
ms.topic: function
req.header: avrt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Avrt.lib
req.dll: Avrt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avrt.dll
api_name:
 - AvRtLeaveThreadOrderingGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AvRtLeaveThreadOrderingGroup function


## -description


Enables client threads to leave a thread ordering group.


## -parameters




### -param Context [in]

A context handle. This handle is returned by the <a href="https://msdn.microsoft.com/76e70f91-750e-49c8-8ddf-e8eddd150aa4">AvRtJoinThreadOrderingGroup</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The parent thread for a thread ordering group should not remove itself from the group.

If a thread times out and attempts to call this function, the function fails with a last error code of ERROR_INVALID_PARAMETER.




## -see-also




<a href="https://msdn.microsoft.com/5c37873a-ced4-447e-a6e1-55cfa8ab24b4">Thread Ordering Service</a>
 

 


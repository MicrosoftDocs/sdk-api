---
UID: NF:lmalert.ALERT_OTHER_INFO
title: ALERT_OTHER_INFO macro
author: windows-sdk-content
description: The ALERT_OTHER_INFO macro returns a pointer to the alert-specific data in an alert message. The data follows a STD_ALERT structure, and can be an ADMIN_OTHER_INFO, a PRINT_OTHER_INFO, or a USER_OTHER_INFO structure.
old-location: netmgmt\alert_other_info.htm
tech.root: NetMgmt
ms.assetid: e7bcc306-4b44-4230-96aa-a4717bb1fb11
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ALERT_OTHER_INFO, ALERT_OTHER_INFO macro [Network Management], _win32_alert_other_info, lmalert/ALERT_OTHER_INFO, netmgmt.alert_other_info
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: lmalert.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Lmalert.h
api_name:
 - ALERT_OTHER_INFO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ALERT_OTHER_INFO macro


## -description


The 
				<b>ALERT_OTHER_INFO</b> macro returns a pointer to the alert-specific data in an alert message. The data follows a 
<a href="https://msdn.microsoft.com/daa4594f-e59e-4f05-8183-677bee4ea446">STD_ALERT</a> structure, and can be an 
<a href="https://msdn.microsoft.com/43119dcf-7d04-4e3b-b1dc-20e814fbdc2f">ADMIN_OTHER_INFO</a>, a 
<a href="https://msdn.microsoft.com/f2fd87bc-abde-43c0-b29d-d43cc5f038b8">PRINT_OTHER_INFO</a>, or a 
<a href="https://msdn.microsoft.com/2f6bd906-fdab-410a-8856-4482e047371f">USER_OTHER_INFO</a> structure.


## -parameters




### -param x

Pointer to a 
<b>STD_ALERT</b> structure that was specified in a call to the 
<a href="https://msdn.microsoft.com/11367a72-c21d-4044-98cf-a7a30cc43a8b">NetAlertRaise</a> function.


## -remarks



The 
<b>ALERT_OTHER_INFO</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;

#define ALERT_OTHER_INFO(x)    ((LPBYTE)(x) + sizeof(STD_ALERT))

</pre>
</td>
</tr>
</table></span></div>
See 
<a href="https://msdn.microsoft.com/11367a72-c21d-4044-98cf-a7a30cc43a8b">NetAlertRaise</a> for a code sample that uses the 
<b>ALERT_OTHER_INFO</b> macro to retrieve a pointer to the 
<b>ADMIN_OTHER_INFO</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/43119dcf-7d04-4e3b-b1dc-20e814fbdc2f">ADMIN_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/ff71fb3d-8c01-47ac-93f2-108b1f49e2da">ALERT_VAR_DATA</a>



<a href="https://msdn.microsoft.com/e131191b-7413-45ff-84cd-b3a873d33ca1">Alert Functions</a>



<a href="https://msdn.microsoft.com/11367a72-c21d-4044-98cf-a7a30cc43a8b">NetAlertRaise</a>



<a href="https://msdn.microsoft.com/b295fae7-0893-4f3b-a414-2fe38f2261b5">Network
		  Management Macros</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/f2fd87bc-abde-43c0-b29d-d43cc5f038b8">PRINT_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/daa4594f-e59e-4f05-8183-677bee4ea446">STD_ALERT</a>



<a href="https://msdn.microsoft.com/2f6bd906-fdab-410a-8856-4482e047371f">USER_OTHER_INFO</a>
 

 


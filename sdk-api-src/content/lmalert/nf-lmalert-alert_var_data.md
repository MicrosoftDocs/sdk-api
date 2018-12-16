---
UID: NF:lmalert.ALERT_VAR_DATA
title: ALERT_VAR_DATA macro
author: windows-sdk-content
description: The ALERT_VAR_DATA macro returns a pointer to the variable-length portion of an alert message. Variable-length data can follow an ADMIN_OTHER_INFO, a PRINT_OTHER_INFO, or a USER_OTHER_INFO structure.
old-location: netmgmt\alert_var_data.htm
tech.root: netmgmt
ms.assetid: ff71fb3d-8c01-47ac-93f2-108b1f49e2da
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ALERT_VAR_DATA, ALERT_VAR_DATA macro [Network Management], _win32_alert_var_data, lmalert/ALERT_VAR_DATA, netmgmt.alert_var_data
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
 - ALERT_VAR_DATA
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ALERT_VAR_DATA macro


## -description


The 
				<b>ALERT_VAR_DATA</b> macro returns a pointer to the variable-length portion of an alert message. Variable-length data can follow an 
<a href="https://msdn.microsoft.com/43119dcf-7d04-4e3b-b1dc-20e814fbdc2f">ADMIN_OTHER_INFO</a>, a 
<a href="https://msdn.microsoft.com/f2fd87bc-abde-43c0-b29d-d43cc5f038b8">PRINT_OTHER_INFO</a>, or a 
<a href="https://msdn.microsoft.com/2f6bd906-fdab-410a-8856-4482e047371f">USER_OTHER_INFO</a> structure.


## -parameters




### -param p

Pointer to an 
<b>ADMIN_OTHER_INFO</b>, a 
<b>PRINT_OTHER_INFO</b>, or a 
<b>USER_OTHER_INFO</b> structure that was specified in a call to the 
<a href="https://msdn.microsoft.com/11367a72-c21d-4044-98cf-a7a30cc43a8b">NetAlertRaise</a> function or the 
<a href="https://msdn.microsoft.com/9762f0d6-0022-4e05-b2d8-6223d7bbb2c8">NetAlertRaiseEx</a> function.


## -remarks



The 
<b>ALERT_VAR_DATA</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;

#define ALERT_VAR_DATA(p)      ((LPBYTE)(p) + sizeof(*p))

</pre>
</td>
</tr>
</table></span></div>
See 
<a href="https://msdn.microsoft.com/11367a72-c21d-4044-98cf-a7a30cc43a8b">NetAlertRaise</a> and 
<a href="https://msdn.microsoft.com/9762f0d6-0022-4e05-b2d8-6223d7bbb2c8">NetAlertRaiseEx</a> for code samples that use the 
<b>ALERT_VAR_DATA</b> macro to retrieve a pointer to the variable-length data in an alert message.




## -see-also




<a href="https://msdn.microsoft.com/43119dcf-7d04-4e3b-b1dc-20e814fbdc2f">ADMIN_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/e7bcc306-4b44-4230-96aa-a4717bb1fb11">ALERT_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/e131191b-7413-45ff-84cd-b3a873d33ca1">Alert Functions</a>



<a href="https://msdn.microsoft.com/11367a72-c21d-4044-98cf-a7a30cc43a8b">NetAlertRaise</a>



<a href="https://msdn.microsoft.com/9762f0d6-0022-4e05-b2d8-6223d7bbb2c8">NetAlertRaiseEx</a>



<a href="https://msdn.microsoft.com/b295fae7-0893-4f3b-a414-2fe38f2261b5">Network
		  Management Macros</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/f2fd87bc-abde-43c0-b29d-d43cc5f038b8">PRINT_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/2f6bd906-fdab-410a-8856-4482e047371f">USER_OTHER_INFO</a>
 

 


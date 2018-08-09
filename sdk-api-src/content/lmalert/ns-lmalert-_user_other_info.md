---
UID: NS:lmalert._USER_OTHER_INFO
title: "_USER_OTHER_INFO"
author: windows-sdk-content
description: The USER_OTHER_INFO structure contains user error code information. The NetAlertRaise and NetAlertRaiseEx functions use the USER_OTHER_INFO structure to specify information about an event or condition of interest to a user.
old-location: netmgmt\user_other_info_str.htm
old-project: netmgmt
ms.assetid: 2f6bd906-fdab-410a-8856-4482e047371f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPUSER_OTHER_INFO, *PUSER_OTHER_INFO, LPUSER_OTHER_INFO, LPUSER_OTHER_INFO structure pointer [Network Management], PUSER_OTHER_INFO, PUSER_OTHER_INFO structure pointer [Network Management], USER_OTHER_INFO, USER_OTHER_INFO structure [Network Management], _USER_OTHER_INFO, _win32_user_other_info_str, lmalert/LPUSER_OTHER_INFO, lmalert/PUSER_OTHER_INFO, lmalert/USER_OTHER_INFO, netmgmt.user_other_info_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: USER_OTHER_INFO, *PUSER_OTHER_INFO, *LPUSER_OTHER_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmalert.h
api_name:
 - USER_OTHER_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _USER_OTHER_INFO structure


## -description


The
				<b>USER_OTHER_INFO</b> structure contains user error code information. The 
<a href="https://msdn.microsoft.com/11367a72-c21d-4044-98cf-a7a30cc43a8b">NetAlertRaise</a> and 
<a href="https://msdn.microsoft.com/9762f0d6-0022-4e05-b2d8-6223d7bbb2c8">NetAlertRaiseEx</a> functions use the 
<b>USER_OTHER_INFO</b> structure to specify information about an event or condition of interest to a user.


## -struct-fields




### -field alrtus_errcode

Specifies the error code for the new message in the message log.


### -field alrtus_numstrings

Specifies the number (0-9) of consecutive Unicode strings in the message log.


## -remarks



Additional variable-length data follows the 
<b>USER_OTHER_INFO</b> structure in the alert message buffer. The information is in the form of contiguous null-terminated character strings, as follows.

<table>
<tr>
<th>String</th>
<th>Meaning</th>
</tr>
<tr>
<td>username</td>
<td>The user who created the session.</td>
</tr>
<tr>
<td>computername</td>
<td>The computer that created the session.</td>
</tr>
</table>
 


<div> </div>


The calling application must allocate and free the memory for all structures and variable-length data in an alert message buffer.

See 
<a href="https://msdn.microsoft.com/9762f0d6-0022-4e05-b2d8-6223d7bbb2c8">NetAlertRaiseEx</a> for a code sample that demonstrates how to raise a user alert.




## -see-also




<a href="https://msdn.microsoft.com/43119dcf-7d04-4e3b-b1dc-20e814fbdc2f">ADMIN_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/e131191b-7413-45ff-84cd-b3a873d33ca1">Alert Functions</a>



<a href="https://msdn.microsoft.com/832ebe88-e1c4-4ce3-8057-922419b577f7">ERRLOG_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/11367a72-c21d-4044-98cf-a7a30cc43a8b">NetAlertRaise</a>



<a href="https://msdn.microsoft.com/9762f0d6-0022-4e05-b2d8-6223d7bbb2c8">NetAlertRaiseEx</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/f2fd87bc-abde-43c0-b29d-d43cc5f038b8">PRINT_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/daa4594f-e59e-4f05-8183-677bee4ea446">STD_ALERT</a>
 

 


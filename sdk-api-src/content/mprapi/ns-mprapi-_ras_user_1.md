---
UID: NS:mprapi._RAS_USER_1
title: "_RAS_USER_1"
author: windows-sdk-content
description: The RAS_USER_1 structure contains information for a particular Remote Access Service user. The RAS_USER_1 structure is similar to the RAS_USER_0 structure, except that RAS_USER_1 supports an additional member, bfPrivilege2.
old-location: rras\ras_user_1.htm
tech.root: RRAS
ms.assetid: 4699346e-0ed0-4091-a8d5-8a12cd6bfbcf
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PRAS_USER_1, PRAS_USER_1, PRAS_USER_1 structure pointer [RAS], RASPRIV2_DialinPolicy, RASPRIV_AdminSetCallback, RASPRIV_CallerSetCallback, RASPRIV_DialinPrivilege, RASPRIV_NoCallback, RAS_USER_1, RAS_USER_1 structure [RAS], _RAS_USER_1, _mpr_ras_user_1, mprapi/PRAS_USER_1, mprapi/RAS_USER_1, rras.ras_user_1"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mprapi.h
req.include-header: 
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
 - Mprapi.h
api_name:
 - RAS_USER_1
product: Windows
targetos: Windows
req.typenames: RAS_USER_1, *PRAS_USER_1
req.redist: 
---

# _RAS_USER_1 structure


## -description


The 
<b>RAS_USER_1</b> structure contains information for a particular Remote Access Service user. The 
<b>RAS_USER_1</b> structure is similar to the 
<a href="https://msdn.microsoft.com/f034c6c2-2dac-40bf-b810-9bf6f3eb3c41">RAS_USER_0</a> structure, except that 
<b>RAS_USER_1</b> supports an additional member, <b>bfPrivilege2</b>.


## -struct-fields




### -field bfPrivilege

Specifies the types of remote access privilege available to the RAS user. 




The following remote access privilege constants are defined in Mprapi.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASPRIV_DialinPrivilege"></a><a id="raspriv_dialinprivilege"></a><a id="RASPRIV_DIALINPRIVILEGE"></a><dl>
<dt><b>RASPRIV_DialinPrivilege</b></dt>
</dl>
</td>
<td width="60%">
The user has permission to dial in to the RAS server.

</td>
</tr>
<tr>
<td width="40%"><a id="RASPRIV_NoCallback"></a><a id="raspriv_nocallback"></a><a id="RASPRIV_NOCALLBACK"></a><dl>
<dt><b>RASPRIV_NoCallback</b></dt>
</dl>
</td>
<td width="60%">
The RAS server will not call back the user to establish a connection.

</td>
</tr>
<tr>
<td width="40%"><a id="RASPRIV_AdminSetCallback"></a><a id="raspriv_adminsetcallback"></a><a id="RASPRIV_ADMINSETCALLBACK"></a><dl>
<dt><b>RASPRIV_AdminSetCallback</b></dt>
</dl>
</td>
<td width="60%">
When the user calls, the RAS server hangs up and calls a preset call-back phone number stored in the user account database. The <b>wszPhoneNumber</b> member of the 
<a href="https://msdn.microsoft.com/a2d4a935-f46d-4bc2-ada8-beaa3ac74834">RAS_USER_0</a> structure contains the user's call-back phone number.

</td>
</tr>
<tr>
<td width="40%"><a id="RASPRIV_CallerSetCallback"></a><a id="raspriv_callersetcallback"></a><a id="RASPRIV_CALLERSETCALLBACK"></a><dl>
<dt><b>RASPRIV_CallerSetCallback</b></dt>
</dl>
</td>
<td width="60%">
When the user calls, the RAS server provides the option of specifying a call-back phone number. The user can also choose to connect immediately without a call back. The <b>wszPhoneNumber</b> member contains a default number that the user can override.

</td>
</tr>
</table>
 


<div> </div>


Use the following constant as a mask to isolate the call back privilege. (This constant is also defined in Mprapi.h.)

RASPRIV_CallbackType


### -field wszPhoneNumber

Pointer to a Unicode string containing the phone number at which the RAS user should be called back.


### -field bfPrivilege2

Specifies flags that grant additional remote access privileges to the RAS user. 




The following remote access privilege constants are defined in Mprapi.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASPRIV2_DialinPolicy"></a><a id="raspriv2_dialinpolicy"></a><a id="RASPRIV2_DIALINPOLICY"></a><dl>
<dt><b>RASPRIV2_DialinPolicy</b></dt>
</dl>
</td>
<td width="60%">
Remote access policies determine whether the user is allowed dial-in access.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/d04f6925-ac38-4adf-ac2e-701db5435c90">MprAdminUserGetInfo</a>



<a href="https://msdn.microsoft.com/7f4d5213-56b4-43d2-93c8-ee5ca50b2a19">MprAdminUserSetInfo</a>



<a href="https://msdn.microsoft.com/858fcdd8-6587-41c4-a2d7-c871722562e7">RAS
		  Administration Structures</a>



<a href="https://msdn.microsoft.com/f034c6c2-2dac-40bf-b810-9bf6f3eb3c41">RAS_USER_0</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 


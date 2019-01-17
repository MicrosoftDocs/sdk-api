---
UID: NS:rasshost._SECURITY_MESSAGE
title: SECURITY_MESSAGE
author: windows-sdk-content
description: The SECURITY_MESSAGE structure is used with the RasSecurityDialogComplete function to indicate the results of a RAS security DLL authentication transaction.
old-location: rras\security_message_str.htm
tech.root: RRAS
ms.assetid: 7eab7bff-1c72-4382-980f-be4e58d60159
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSECURITY_MESSAGE, PSECURITY_MESSAGE, PSECURITY_MESSAGE structure pointer [RAS], SECURITYMSG_ERROR, SECURITYMSG_FAILURE, SECURITYMSG_SUCCESS, SECURITY_MESSAGE, SECURITY_MESSAGE structure [RAS], _ras_security_message_str, rasshost/PSECURITY_MESSAGE, rasshost/SECURITY_MESSAGE, rras.security_message_str"
ms.topic: struct
req.header: rasshost.h
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
 - Rasshost.h
api_name:
 - SECURITY_MESSAGE
product: Windows
targetos: Windows
req.typenames: SECURITY_MESSAGE, *PSECURITY_MESSAGE
req.redist: 
---

# SECURITY_MESSAGE structure


## -description


The 
<b>SECURITY_MESSAGE</b> structure is used with the 
<a href="https://msdn.microsoft.com/9ebe8b85-7500-405f-98c2-6f51f3339629">RasSecurityDialogComplete</a> function to indicate the results of a RAS security DLL authentication transaction.


## -struct-fields




### -field dwMsgId

Indicates whether the RAS server should grant access to the remote user. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECURITYMSG_SUCCESS"></a><a id="securitymsg_success"></a><dl>
<dt><b>SECURITYMSG_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The security DLL successfully authenticated the remote user identified by the <b>UserName</b> member. The RAS server  proceeds with its PPP authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="SECURITYMSG_FAILURE"></a><a id="securitymsg_failure"></a><dl>
<dt><b>SECURITYMSG_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The security DLL denied access to the remote user identified by the <b>UserName</b> member. The RAS server  hangs up the call and records the failed authentication in the event log.

</td>
</tr>
<tr>
<td width="40%"><a id="SECURITYMSG_ERROR"></a><a id="securitymsg_error"></a><dl>
<dt><b>SECURITYMSG_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred that prevented validation of the remote user. The RAS server  hangs up the call and records the error in the event log.

</td>
</tr>
</table>
 


### -field hPort

Specifies the port handle that the RAS server passed to the security DLL in the 
<a href="https://msdn.microsoft.com/19f4591b-ecae-478b-b110-c0d88c72f7eb">RasSecurityDialogBegin</a> call for this authentication transaction.


### -field dwError

Specifies an error code. If <b>dwMsgId</b> is SECURITYMSG_ERROR, set <b>dwError</b> to one of the nonzero error codes defined in Winerror.h or Raserror.h. The RAS server records this error code in the event log. If the <b>dwMsgId</b> member indicates success or failure, set <b>dwError</b> to zero.


### -field UserName

Specifies the name of the remote user if <b>dwMsgId</b> is SECURITYMSG_SUCCESS or SECURITYMSG_FAILURE. This string can be empty if <b>dwMsgId</b> is SECURITYMSG_ERROR.


### -field Domain

Specifies the name of the logon domain for the remote user if <b>dwMsgId</b> is SECURITYMSG_SUCCESS or SECURITYMSG_FAILURE. This string can be empty if <b>dwMsgId</b> is SECURITYMSG_ERROR.


## -see-also




<a href="https://msdn.microsoft.com/b04bef8c-a83e-4c6e-849e-feeca99699e8">RAS Server Administration Structures</a>



<a href="https://msdn.microsoft.com/19f4591b-ecae-478b-b110-c0d88c72f7eb">RasSecurityDialogBegin</a>



<a href="https://msdn.microsoft.com/9ebe8b85-7500-405f-98c2-6f51f3339629">RasSecurityDialogComplete</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>
 

 


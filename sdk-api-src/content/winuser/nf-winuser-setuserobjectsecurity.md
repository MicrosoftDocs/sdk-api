---
UID: NF:winuser.SetUserObjectSecurity
title: SetUserObjectSecurity function
author: windows-sdk-content
description: Sets the security of a user object. This can be, for example, a window or a DDE conversation.
old-location: security\setuserobjectsecurity.htm
tech.root: secauthz
ms.assetid: 219e41b8-9ac7-4747-a585-b6b9df6a1c9c
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: DACL_SECURITY_INFORMATION, GROUP_SECURITY_INFORMATION, OWNER_SECURITY_INFORMATION, SACL_SECURITY_INFORMATION, SetUserObjectSecurity, SetUserObjectSecurity function [Security], _win32_setuserobjectsecurity, security.setuserobjectsecurity, winuser/SetUserObjectSecurity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - SetUserObjectSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetUserObjectSecurity function


## -description


The <b>SetUserObjectSecurity</b> function sets the security of a user object. This can be, for example, a window or a DDE conversation.


## -parameters




### -param hObj [in]

A handle to a user object for which security information is set.


### -param pSIRequested [in]

A pointer to a value that indicates the components of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> to set. This parameter can be a combination of the following values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DACL_SECURITY_INFORMATION"></a><a id="dacl_security_information"></a><dl>
<dt><b>DACL_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Sets the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) of the object. The handle specified by <i>hObj</i>  must have WRITE_DAC access, or the calling <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a> must be the owner of the object.

</td>
</tr>
<tr>
<td width="40%"><a id="GROUP_SECURITY_INFORMATION"></a><a id="group_security_information"></a><dl>
<dt><b>GROUP_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Sets the primary group <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) of the object.

</td>
</tr>
<tr>
<td width="40%"><a id="OWNER_SECURITY_INFORMATION"></a><a id="owner_security_information"></a><dl>
<dt><b>OWNER_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Sets the SID of the owner of the object. The handle specified by <i>hObj</i>  must have WRITE_OWNER access, or the calling process must be the owner of the object or have the SE_TAKE_OWNERSHIP_NAME privilege enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="SACL_SECURITY_INFORMATION"></a><a id="sacl_security_information"></a><dl>
<dt><b>SACL_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Sets the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) of the object. The handle specified by <i>hObj</i>  must have ACCESS_SYSTEM_SECURITY access. 

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To obtain ACCESS_SYSTEM_SECURITY access</b>

<ol>
<li>Enable the SE_SECURITY_NAME 
<a href="https://msdn.microsoft.com/fe6aae0f-93eb-4aba-a6ac-45e71c251c51">privilege</a> in the current <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> of the caller.</li>
<li>Open the handle for ACCESS_SYSTEM_SECURITY access. </li>
<li>Disable the privilege.</li>
</ol>
</td>
</tr>
</table>
 


### -param pSID [in]

A pointer to a 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure that contains the new security information. 




This buffer must be aligned on a 4-byte boundary.  


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>SetUserObjectSecurity</b> function applies changes specified in a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> to the security descriptor assigned to a user object. The security descriptor of the object must be in <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">self-relative</a> form. If necessary, this function allocates additional memory to increase the size of the security descriptor.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/9e9ed9b7-ea23-4dec-8b92-a86aa81267ab">Starting an Interactive Client Process</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/998c2520-7833-4efd-a794-b13b528f0485">GetUserObjectSecurity</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/27766c97-7ac5-40fc-b798-7cd07e496c0d">SetFileSecurity</a>



<a href="https://msdn.microsoft.com/2a70483e-245d-4bc7-b90a-58d143364ce1">SetKernelObjectSecurity</a>



<a href="https://msdn.microsoft.com/726994c8-7813-4f1a-b7d7-a25e79202c33">SetPrivateObjectSecurity</a>
 

 


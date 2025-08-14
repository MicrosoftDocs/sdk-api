---
UID: NF:winuser.SetUserObjectSecurity
title: SetUserObjectSecurity function (winuser.h)
description: Sets the security of a user object. This can be, for example, a window or a DDE conversation.
helpviewer_keywords: ["DACL_SECURITY_INFORMATION","GROUP_SECURITY_INFORMATION","OWNER_SECURITY_INFORMATION","SACL_SECURITY_INFORMATION","SetUserObjectSecurity","SetUserObjectSecurity function [Security]","_win32_setuserobjectsecurity","security.setuserobjectsecurity","winuser/SetUserObjectSecurity"]
old-location: security\setuserobjectsecurity.htm
tech.root: security
ms.assetid: 219e41b8-9ac7-4747-a585-b6b9df6a1c9c
ms.date: 12/05/2018
ms.keywords: DACL_SECURITY_INFORMATION, GROUP_SECURITY_INFORMATION, OWNER_SECURITY_INFORMATION, SACL_SECURITY_INFORMATION, SetUserObjectSecurity, SetUserObjectSecurity function [Security], _win32_setuserobjectsecurity, security.setuserobjectsecurity, winuser/SetUserObjectSecurity
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetUserObjectSecurity
 - winuser/SetUserObjectSecurity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-usersecurity-l1-1-0.dll
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
---

# SetUserObjectSecurity function


## -description

The <b>SetUserObjectSecurity</b> function sets the security of a user object. This can be, for example, a window or a DDE conversation.

## -parameters

### -param hObj [in]

A handle to a user object for which security information is set.

### -param pSIRequested [in]

A pointer to a value that indicates the components of the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> to set. This parameter can be a combination of the following values. 




					

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
Sets the <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) of the object. The handle specified by <i>hObj</i>  must have WRITE_DAC access, or the calling <a href="/windows/desktop/SecGloss/p-gly">process</a> must be the owner of the object.

</td>
</tr>
<tr>
<td width="40%"><a id="GROUP_SECURITY_INFORMATION"></a><a id="group_security_information"></a><dl>
<dt><b>GROUP_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Sets the primary group <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) of the object.

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
Sets the <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) of the object. The handle specified by <i>hObj</i>  must have ACCESS_SYSTEM_SECURITY access. 

<p class="proch"><b>To obtain ACCESS_SYSTEM_SECURITY access</b>

<ol>
<li>Enable the SE_SECURITY_NAME 
<a href="/windows/desktop/SecAuthZ/privileges">privilege</a> in the current <a href="/windows/desktop/SecGloss/a-gly">access token</a> of the caller.</li>
<li>Open the handle for ACCESS_SYSTEM_SECURITY access. </li>
<li>Disable the privilege.</li>
</ol>
</td>
</tr>
</table>

### -param pSID [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that contains the new security information. 




This buffer must be aligned on a 4-byte boundary.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>SetUserObjectSecurity</b> function applies changes specified in a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> to the security descriptor assigned to a user object. The security descriptor of the object must be in <a href="/windows/desktop/SecGloss/s-gly">self-relative</a> form. If necessary, this function allocates additional memory to increase the size of the security descriptor.


#### Examples

For an example that uses this function, see <a href="/previous-versions/aa379608(v=vs.85)">Starting an Interactive Client Process</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity">GetUserObjectSecurity</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setfilesecuritya">SetFileSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity">SetKernelObjectSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity">SetPrivateObjectSecurity</a>
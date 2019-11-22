---
UID: NF:winbase.LookupPrivilegeValueA
title: LookupPrivilegeValueA function (winbase.h)

description: Retrieves the locally unique identifier (LUID) used on a specified system to locally represent the specified privilege name.
old-location: security\lookupprivilegevalue.htm
tech.root: SecAuthZ
ms.assetid: 334b8ba8-101d-43a1-a8bf-1c7e0448c272

ms.date: 12/05/2018
ms.keywords: LookupPrivilegeValue, LookupPrivilegeValue function [Security], LookupPrivilegeValueA, LookupPrivilegeValueW, _win32_lookupprivilegevalue, security.lookupprivilegevalue, winbase/LookupPrivilegeValue, winbase/LookupPrivilegeValueA, winbase/LookupPrivilegeValueW
ms.topic: function
f1_keywords: 
 - "winbase/LookupPrivilegeValue"
dev_langs:
 - c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LookupPrivilegeValueW (Unicode) and LookupPrivilegeValueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-security-lsalookup-l2-1-0.dll
 - API-MS-Win-security-lsalookup-l2-1-1.dll
 - Ext-MS-Win-AdvAPI32-auth-l1-1-0.dll
 - API-MS-Win-Security-LSALookup-L2-1-2.dll
 - API-MS-Win-Security-LSALookup-Ansi-L2-1-0.dll
api_name:
 - LookupPrivilegeValue
 - LookupPrivilegeValueA
 - LookupPrivilegeValueW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LookupPrivilegeValueA function


## -description


The <b>LookupPrivilegeValue</b> function retrieves the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/l-gly">locally unique identifier</a> (LUID) used on a specified system to locally represent the specified privilege name.
		


## -parameters




### -param lpSystemName [in, optional]

A pointer to a null-terminated string that specifies the name of the system on which the privilege name is retrieved. If a null string is specified, the function attempts to find the privilege name on the local system.


### -param lpName [in]

A pointer to a null-terminated string that specifies the name of the privilege, as defined in the Winnt.h header file. For example, this parameter could specify the constant, SE_SECURITY_NAME, or its corresponding string, "SeSecurityPrivilege".


### -param lpLuid [out]

A pointer to a variable that receives the LUID by which the privilege is known on the system specified by the <i>lpSystemName</i> parameter.


## -returns



If the function succeeds, the function returns nonzero.
						

If the function fails, it returns zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The <b>LookupPrivilegeValue</b> function supports only the privileges specified in the Defined Privileges section of Winnt.h. For a list of values, see <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/privilege-constants">Privilege Constants</a>.


#### Examples

For an example that uses this function, see <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--">Enabling and Disabling Privileges</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-lookupprivilegedisplaynamea">LookupPrivilegeDisplayName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-lookupprivilegenamea">LookupPrivilegeName</a>
 

 


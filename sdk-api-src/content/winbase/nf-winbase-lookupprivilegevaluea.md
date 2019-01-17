---
UID: NF:winbase.LookupPrivilegeValueA
title: LookupPrivilegeValueA function
author: windows-sdk-content
description: Retrieves the locally unique identifier (LUID) used on a specified system to locally represent the specified privilege name.
old-location: security\lookupprivilegevalue.htm
tech.root: SecAuthZ
ms.assetid: 334b8ba8-101d-43a1-a8bf-1c7e0448c272
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: LookupPrivilegeValue, LookupPrivilegeValue function [Security], LookupPrivilegeValueA, LookupPrivilegeValueW, _win32_lookupprivilegevalue, security.lookupprivilegevalue, winbase/LookupPrivilegeValue, winbase/LookupPrivilegeValueA, winbase/LookupPrivilegeValueW
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LookupPrivilegeValueA function


## -description


The <b>LookupPrivilegeValue</b> function retrieves the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">locally unique identifier</a> (LUID) used on a specified system to locally represent the specified privilege name.
		


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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>LookupPrivilegeValue</b> function supports only the privileges specified in the Defined Privileges section of Winnt.h. For a list of values, see <a href="https://msdn.microsoft.com/973796a6-bc2e-4e64-92db-5e17b9c25460">Privilege Constants</a>.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/aa2d3fe7-01ee-4243-b72c-3e8b90068e22">Enabling and Disabling Privileges</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/1fbb26b6-615e-4883-9f4b-3a1d05d9feaa">LookupPrivilegeDisplayName</a>



<a href="https://msdn.microsoft.com/580fb58f-1470-4389-9f07-8f37403e2bdf">LookupPrivilegeName</a>
 

 


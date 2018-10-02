---
UID: NF:winbase.LookupPrivilegeNameA
title: LookupPrivilegeNameA function
author: windows-sdk-content
description: Retrieves the name that corresponds to the privilege represented on a specific system by a specified locally unique identifier (LUID).
old-location: security\lookupprivilegename.htm
tech.root: SecAuthZ
ms.assetid: 580fb58f-1470-4389-9f07-8f37403e2bdf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: LookupPrivilegeName, LookupPrivilegeName function [Security], LookupPrivilegeNameA, LookupPrivilegeNameW, _win32_lookupprivilegename, security.lookupprivilegename, winbase/LookupPrivilegeName, winbase/LookupPrivilegeNameA, winbase/LookupPrivilegeNameW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LookupPrivilegeNameW (Unicode) and LookupPrivilegeNameA (ANSI)
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
 - API-MS-Win-Security-LSALookup-L2-1-2.dll
 - API-MS-Win-Security-LSALookup-Ansi-L2-1-0.dll
api_name:
 - LookupPrivilegeName
 - LookupPrivilegeNameA
 - LookupPrivilegeNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LookupPrivilegeNameA function


## -description


The <b>LookupPrivilegeName</b> function retrieves the name that corresponds to the privilege represented on a specific system by a specified <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">locally unique identifier</a> (LUID).


## -parameters




### -param lpSystemName [in, optional]

A pointer to a null-terminated string that specifies the name of the system on which the privilege name is retrieved. If a null string is specified, the function attempts to find the privilege name on the local system.


### -param lpLuid [in]

A pointer to the LUID by which the privilege is known on the target system.


### -param lpName [out, optional]

A pointer to a buffer that receives a null-terminated string that represents the privilege name. For example, this string could be "SeSecurityPrivilege".


### -param cchName [in, out]

A pointer to a variable that specifies the size, in a <b>TCHAR</b> value, of the <i>lpName</i> buffer. When the function returns, this parameter contains the length of the privilege name, not including the terminating null character. If the buffer pointed to by the <i>lpName</i> parameter is too small, this variable contains the required size.


## -returns



If the function succeeds, the function returns nonzero.
						

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>LookupPrivilegeName</b> function supports only the privileges specified in the Defined Privileges section of Winnt.h. For a list of values, see <a href="https://msdn.microsoft.com/973796a6-bc2e-4e64-92db-5e17b9c25460">Privilege Constants</a>.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/1fbb26b6-615e-4883-9f4b-3a1d05d9feaa">LookupPrivilegeDisplayName</a>



<a href="https://msdn.microsoft.com/334b8ba8-101d-43a1-a8bf-1c7e0448c272">LookupPrivilegeValue</a>
 

 


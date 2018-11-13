---
UID: NC:winfax.PFAXACCESSCHECK
title: PFAXACCESSCHECK
author: windows-sdk-content
description: A fax client application calls the FaxAccessCheck function to query the fax access privileges of a user.
old-location: fax\_mfax_faxaccesscheck.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_76i3.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: FaxAccessCheckA, FaxAccessCheckW, PFAXACCESSCHECK, PFAXACCESSCHECK callback, PFAXACCESSCHECK callback function [Fax Service], _mfax_faxaccesscheck, fax._mfax_faxaccesscheck, winfax/FaxAccessCheckA, winfax/FaxAccessCheckW, winfax/PFAXACCESSCHECK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxAccessCheckW (Unicode) and FaxAccessCheckA (ANSI)
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
 - UserDefined
api_location:
 - Winfax.h
api_name:
 - PFAXACCESSCHECK
 - FaxAccessCheckA
 - FaxAccessCheckW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFAXACCESSCHECK callback function


## -description


A fax client application calls the <b>FaxAccessCheck</b> function to query the fax access privileges of a user.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms691482(v=VS.85).aspx">FaxConnectFaxServer</a> function.


### -param AccessMask [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that contains a set of bit flags defining a user's fax access permissions. This parameter can be one or more of the following generic access permissions: FAX_READ, FAX_WRITE, and FAX_ALL_ACCESS. It can also be one or more of the following specific access permissions:

                    


<ul>
<li>FAX_JOB_SUBMIT</li>
<li>FAX_JOB_QUERY</li>
<li>FAX_CONFIG_QUERY</li>
<li>FAX_CONFIG_SET</li>
<li>FAX_PORT_QUERY</li>
<li>FAX_PORT_SET</li>
<li>FAX_JOB_MANAGE</li>
</ul>


For a detailed description of these values, see <a href="https://msdn.microsoft.com/en-us/library/ms691834(v=VS.85).aspx">Generic Fax Access Rights</a> and <a href="https://msdn.microsoft.com/en-us/library/ms692302(v=VS.85).aspx">Specific Fax Access Rights</a>.


## -returns



Type: <b>BOOL</b>

If the user has the required permission, the return value is nonzero.

If the user does not have the required permission, the return value is zero, and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_SUCCESS.

If the function fails, the return value is also zero, but <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns an error code other than ERROR_SUCCESS.




## -remarks



The fax service is a secure service. Users must have certain access privileges to successfully call fax service functions. Call the <b>FaxAccessCheck</b> function to programmatically check a user's fax access permissions. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms692808(v=VS.85).aspx">Checking the Access Rights of Users</a> and <a href="https://msdn.microsoft.com/en-us/library/ms692351(v=VS.85).aspx">Fax Client User Access Rights</a>.

The fax service administration application, a Microsoft Management Console (MMC) snap-in component, is also available for users to query and modify job access, port access, and global configuration data access privileges.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691947(v=VS.85).aspx">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691482(v=VS.85).aspx">FaxConnectFaxServer</a>
 

 


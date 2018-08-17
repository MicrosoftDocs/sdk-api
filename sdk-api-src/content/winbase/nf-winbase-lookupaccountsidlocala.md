---
UID: NF:winbase.LookupAccountSidLocalA
title: LookupAccountSidLocalA function
author: windows-sdk-content
description: Retrieves the name of the account for the specified SID on the local machine.
old-location: security\lookupaccountsidlocal.htm
old-project: secauthz
ms.assetid: B039FFD7-B483-4CC0-B606-FAA5003DA238
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: LookupAccountSidLocal, LookupAccountSidLocal function [Security], LookupAccountSidLocalA, LookupAccountSidLocalW, security.lookupaccountsidlocal, winbase/LookupAccountSidLocal, winbase/LookupAccountSidLocalA, winbase/LookupAccountSidLocalW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LookupAccountSidLocalW (Unicode) and LookupAccountSidLocalA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - api-ms-win-security-lsalookup-l1-1-0.dll
api_name:
 - LookupAccountSidLocal
 - LookupAccountSidLocalA
 - LookupAccountSidLocalW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# LookupAccountSidLocalA function


## -description


Retrieves the name of the account for the specified SID on the local machine.


## -parameters




### -param Sid [in]

A pointer to the 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> to look up.


### -param Name [out, optional]

A pointer to a buffer that receives a <b>null</b>-terminated string that contains the account name that corresponds to the <i>lpSid</i> parameter.


### -param cchName

TBD


### -param ReferencedDomainName [out, optional]

On input, specifies the size, in <b>TCHAR</b>s, of the <i>lpName</i> buffer. If the function fails because the buffer is too small or if <i>cchName</i> is zero, <i>cchName</i> receives the required buffer size, including the terminating <b>null</b> character.

A pointer to a buffer that receives a <b>null</b>-terminated string that contains the name of the domain where the account name was found.

On a server, the domain name returned for most accounts in the security database of the local computer is the name of the domain for which the server is a domain controller.
						

On a workstation, the domain name returned for most accounts in the security database of the local computer is the name of the computer as of the last start of the system (backslashes are excluded). If the name of the computer changes, the old name continues to be returned as the domain name until the system is restarted.

Some accounts are predefined by the system. The domain name returned for these accounts is BUILTIN.


### -param cchReferencedDomainName [in, out]

On input, specifies the size, in <b>TCHAR</b>s, of the <i>lpReferencedDomainName</i> buffer. If the function fails because the buffer is too small or if <i>cchReferencedDomainName</i> is zero, <i>cchReferencedDomainName</i> receives the required buffer size, including the terminating <b>null</b> character.


### -param peUse [out]

A pointer to a variable that receives a 
<a href="https://msdn.microsoft.com/4e6af6bd-056b-4f5a-b223-57a673c3fcfa">SID_NAME_USE</a> value that indicates the type of the account.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function is similar to <a href="https://msdn.microsoft.com/b8a44ffc-86e1-4f79-ad51-8340da9eaefd">LookupAccountSid</a>, but restricts the search to the local machine.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/ef41de63-4ab5-40c6-8b16-b960e1308b5b">EqualPrefixSid</a>



<a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>



<a href="https://msdn.microsoft.com/4e6af6bd-056b-4f5a-b223-57a673c3fcfa">SID_NAME_USE</a>
 

 


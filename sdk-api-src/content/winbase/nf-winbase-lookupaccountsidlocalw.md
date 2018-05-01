---
UID: NF:winbase.LookupAccountSidLocalW
title: LookupAccountSidLocalW function
author: windows-driver-content
description: Retrieves the name of the account for the specified SID on the local machine.
old-location: security\lookupaccountsidlocal.htm
old-project: SecAuthZ
ms.assetid: B039FFD7-B483-4CC0-B606-FAA5003DA238
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: LookupAccountSidLocal, LookupAccountSidLocal function [Security], LookupAccountSidLocalA, LookupAccountSidLocalW, security.lookupaccountsidlocal, winbase/LookupAccountSidLocal, winbase/LookupAccountSidLocalA, winbase/LookupAccountSidLocalW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
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
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	api-ms-win-security-lsalookup-l1-1-0.dll
api_name:
-	LookupAccountSidLocal
-	LookupAccountSidLocalA
-	LookupAccountSidLocalW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# LookupAccountSidLocalW function


## -description


Retrieves the name of the account for the specified SID on the local machine.


## -parameters




### -param Sid

TBD


### -param Name

TBD


#### - cchName [in, out]

On input, specifies the size, in <b>TCHAR</b>s, of the <i>lpName</i> buffer. If the function fails because the buffer is too small or if <i>cchName</i> is zero, <i>cchName</i> receives the required buffer size, including the terminating <b>null</b> character.


### -param ReferencedDomainName

TBD


#### - cchReferencedDomainName [in, out]

On input, specifies the size, in <b>TCHAR</b>s, of the <i>lpReferencedDomainName</i> buffer. If the function fails because the buffer is too small or if <i>cchReferencedDomainName</i> is zero, <i>cchReferencedDomainName</i> receives the required buffer size, including the terminating <b>null</b> character.


#### - peUse [out]

A pointer to a variable that receives a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556744">SID_NAME_USE</a> value that indicates the type of the account.


#### - lpName [out, optional]

A pointer to a buffer that receives a <b>null</b>-terminated string that contains the account name that corresponds to the <i>lpSid</i> parameter.


#### - lpReferencedDomainName [out, optional]

A pointer to a buffer that receives a <b>null</b>-terminated string that contains the name of the domain where the account name was found.

On a server, the domain name returned for most accounts in the security database of the local computer is the name of the domain for which the server is a domain controller.
						

On a workstation, the domain name returned for most accounts in the security database of the local computer is the name of the computer as of the last start of the system (backslashes are excluded). If the name of the computer changes, the old name continues to be returned as the domain name until the system is restarted.

Some accounts are predefined by the system. The domain name returned for these accounts is BUILTIN.


#### - lpSid [in]

A pointer to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> to look up.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function is similar to <a href="https://msdn.microsoft.com/b8a44ffc-86e1-4f79-ad51-8340da9eaefd">LookupAccountSid</a>, but restricts the search to the local machine.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/ef41de63-4ab5-40c6-8b16-b960e1308b5b">EqualPrefixSid</a>



<a href="https://msdn.microsoft.com/72855539-469a-4289-99cc-eae2ed89901f">LookupAccountName</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556744">SID_NAME_USE</a>
 

 


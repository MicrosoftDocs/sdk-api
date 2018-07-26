---
UID: NF:winbase.LookupAccountNameW
title: LookupAccountNameW function
author: windows-sdk-content
description: Accepts the name of a system and an account as input. It retrieves a security identifier (SID) for the account and the name of the domain on which the account was found.
old-location: security\lookupaccountname.htm
old-project: secauthz
ms.assetid: 72855539-469a-4289-99cc-eae2ed89901f
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: LookupAccountName, LookupAccountName function [Security], LookupAccountNameA, LookupAccountNameW, _win32_lookupaccountname, security.lookupaccountname, winbase/LookupAccountName, winbase/LookupAccountNameA, winbase/LookupAccountNameW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LookupAccountNameW (Unicode) and LookupAccountNameA (ANSI)
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
 - API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-security-lsalookup-l2-1-0.dll
 - API-MS-Win-security-lsalookup-l2-1-1.dll
 - API-MS-Win-Security-LSALookup-L2-1-2.dll
 - API-MS-Win-Security-LSALookup-Ansi-L2-1-0.dll
api_name:
 - LookupAccountName
 - LookupAccountNameA
 - LookupAccountNameW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# LookupAccountNameW function


## -description



			The <b>LookupAccountName</b> function accepts the name of a system and an account as input. It retrieves a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) for the account and the name of the domain on which the account was found.

The <a href="https://msdn.microsoft.com/867604aa-7a39-4da7-b189-a9183461e9a0">LsaLookupNames</a> function can also retrieve computer accounts. 


## -parameters




### -param lpSystemName [in, optional]

A pointer to a <b>null</b>-terminated character string that specifies the name of the system. This string can be the name of a remote computer. If this string is <b>NULL</b>, the account name translation begins on the local system. If the name cannot be resolved on the local system, this function will try to resolve the name using domain controllers trusted by the local system. Generally, specify a value for  <i>lpSystemName</i> only when the  account is in an untrusted domain and the   name of a computer in that domain is known.


### -param lpAccountName [in]

A pointer to a <b>null</b>-terminated string that specifies the account name.

Use a fully qualified string in the domain_name\user_name format to ensure that <b>LookupAccountName</b> finds the account in the desired domain.


### -param Sid [out, optional]

A pointer to a buffer that receives the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure that corresponds to the account name pointed to by the <i>lpAccountName</i> parameter. If this parameter is <b>NULL</b>, <i>cbSid</i> must be zero.


### -param cbSid [in, out]

A pointer to a variable. On input, this value specifies the size, in bytes, of the <i>Sid</i> buffer. If the function fails because the buffer is too small or if <i>cbSid</i> is zero, this variable receives the required buffer size.


### -param ReferencedDomainName [out, optional]

A pointer to a buffer that receives the name of the domain where the account name is found. For computers that are not joined to a domain, this buffer receives the computer name. If this parameter is <b>NULL</b>, the function returns the required buffer size.


### -param cchReferencedDomainName [in, out]

A pointer to a variable. On input, this value specifies the size, in <b>TCHAR</b>s, of the <i>ReferencedDomainName</i> buffer. If the function fails because the buffer is too small, this variable receives the required buffer size, including the terminating <b>null</b> character. If the <i>ReferencedDomainName</i> parameter is <b>NULL</b>, this parameter must be zero.


### -param peUse [out]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556744">SID_NAME_USE</a> enumerated type that indicates the type of the account when the function returns.


## -returns




						If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>LookupAccountName</b> function attempts to find a SID for the specified name by first checking a list of well-known SIDs. If the name does not correspond to a well-known SID, the function checks built-in and administratively defined local accounts. Next, the function checks the primary domain. If the name is not found there, trusted domains are checked.

Use fully qualified account names (for example, domain_name\user_name) instead of isolated names (for example, user_name). Fully qualified names are unambiguous and provide better performance when the lookup is performed. This function also supports fully qualified DNS names (for example, example.example.com\user_name) and <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal names</a> (UPN) (for example, someone@example.com).

In addition to looking up local accounts, local domain accounts, and explicitly trusted domain accounts, <b>LookupAccountName</b> can look up the name for any account in any domain in the forest.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/ef41de63-4ab5-40c6-8b16-b960e1308b5b">EqualPrefixSid</a>



<a href="https://msdn.microsoft.com/87adc46a-c069-4ee5-900a-03b646306e64">GetUserName</a>



<a href="https://msdn.microsoft.com/b8a44ffc-86e1-4f79-ad51-8340da9eaefd">LookupAccountSid</a>



<a href="https://msdn.microsoft.com/fe219070-6a00-4b8c-b2e4-2ad290a1cb9c">LsaLookupNames2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556744">SID_NAME_USE</a>
 

 


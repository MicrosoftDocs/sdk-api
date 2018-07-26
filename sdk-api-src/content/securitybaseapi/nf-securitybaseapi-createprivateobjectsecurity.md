---
UID: NF:securitybaseapi.CreatePrivateObjectSecurity
title: CreatePrivateObjectSecurity function
author: windows-sdk-content
description: Allocates and initializes a self-relative security descriptor for a new private object. A protected server calls this function when it creates a new private object.
old-location: security\createprivateobjectsecurity.htm
old-project: secauthz
ms.assetid: 5f4832b6-5cf5-4050-9e20-56674f2e2cb1
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: CreatePrivateObjectSecurity, CreatePrivateObjectSecurity function [Security], _win32_createprivateobjectsecurity, security.createprivateobjectsecurity, securitybaseapi/CreatePrivateObjectSecurity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: securitybaseapi.h
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
tech.root: 
req.typenames: EXTENDED_NAME_FORMAT, *PEXTENDED_NAME_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - CreatePrivateObjectSecurity
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# CreatePrivateObjectSecurity function


## -description


The <b>CreatePrivateObjectSecurity</b> function allocates and initializes a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">self-relative security descriptor</a> for a new private object. A protected server calls this function when it creates a new private object.

To specify the object type GUID of the new object or control how <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) are inherited, use the 
<a href="https://msdn.microsoft.com/edc62121-2625-4ee1-9450-38cb47574bb9">CreatePrivateObjectSecurityEx</a> function.


## -parameters




### -param ParentDescriptor [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> for the parent directory in which a new object is being created. If there is no parent directory, this parameter can be <b>NULL</b>.


### -param CreatorDescriptor [in, optional]

A pointer to a security descriptor provided by the creator of the object. If the object's creator does not explicitly pass security information for the new object, this parameter is intended to be <b>NULL</b>.


### -param NewDescriptor [out]

A pointer to a variable that receives a pointer to the newly allocated self-relative security descriptor. The caller must call the 
<a href="https://msdn.microsoft.com/4ef10852-8229-41de-a4d7-d2845e4c92ce">DestroyPrivateObjectSecurity</a> function to free this security descriptor.


### -param IsDirectoryObject [in]

Specifies whether the new object is a container. A value of <b>TRUE</b> indicates the object contains other objects, such as a directory.


### -param Token [in, optional]

A handle to the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> for the client <a href="https://msdn.microsoft.com/library/windows/hardware/dn756307">process</a> on whose behalf the object is being created. If this is an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>, it must be at SecurityIdentification level or higher. For a full description of the SecurityIdentification impersonation level, see the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556631">SECURITY_IMPERSONATION_LEVEL</a> enumerated type. 




A client token is used to retrieve default security information for the new object, such as its default owner, primary group, and <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a>. The token must be open for <b>TOKEN_QUERY</b> access.

If all of the following conditions are true, then the handle must be opened for <b>TOKEN_DUPLICATE</b> access in addition to <b>TOKEN_QUERY</b> access.

<ul>
<li>The token handle refers to a primary token.</li>
<li>The security descriptor of the token contains one or more ACEs with the <b>OwnerRights</b> SID.</li>
<li>A security descriptor is specified for the <i>CreatorDescriptor</i> parameter.</li>
<li>The caller of this function does not set the <b>SEF_AVOID_OWNER_RESTRICTION</b> flag in the <i>AutoInheritFlags</i> parameter.</li>
</ul>

### -param GenericMapping [in]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546526">GENERIC_MAPPING</a> structure that specifies the mapping from each generic right to specific rights for the object.


## -returns



If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) is specified in the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> specified by the <i>CreatorDescriptor</i> parameter, the <i>Token</i> parameter must have the SE_SECURITY_NAME privilege enabled. The <b>CreatePrivateObjectSecurity</b> function checks this privilege and may generate audits during the process.




## -see-also




<a href="authorization_functions.htm">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>



<a href="https://msdn.microsoft.com/edc62121-2625-4ee1-9450-38cb47574bb9">CreatePrivateObjectSecurityEx</a>



<a href="https://msdn.microsoft.com/4ef10852-8229-41de-a4d7-d2845e4c92ce">DestroyPrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546526">GENERIC_MAPPING</a>



<a href="https://msdn.microsoft.com/3e93c0a0-e449-4df1-812b-c3fb0dfe9c19">GetPrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>



<a href="https://msdn.microsoft.com/1e760ad8-7e46-4748-8c45-36ad8efe936a">OpenProcessToken</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556631">SECURITY_IMPERSONATION_LEVEL</a>



<a href="https://msdn.microsoft.com/726994c8-7813-4f1a-b7d7-a25e79202c33">SetPrivateObjectSecurity</a>
 

 


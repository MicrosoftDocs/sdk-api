---
UID: NF:aclapi.LookupSecurityDescriptorPartsA
title: LookupSecurityDescriptorPartsA function
author: windows-sdk-content
description: Retrieves security information from a self-relative security descriptor.
old-location: security\lookupsecuritydescriptorparts.htm
old-project: secauthz
ms.assetid: 68c3f56b-6c48-4f4b-bd38-9f4e346c663b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LookupSecurityDescriptorParts, LookupSecurityDescriptorParts function [Security], LookupSecurityDescriptorPartsA, LookupSecurityDescriptorPartsW, _win32_lookupsecuritydescriptorparts, aclapi/LookupSecurityDescriptorParts, aclapi/LookupSecurityDescriptorPartsA, aclapi/LookupSecurityDescriptorPartsW, security.lookupsecuritydescriptorparts
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: aclapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LookupSecurityDescriptorPartsW (Unicode) and LookupSecurityDescriptorPartsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRUSTEE_W, *PTRUSTEE_W, TRUSTEEW, *PTRUSTEEW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - LookupSecurityDescriptorParts
 - LookupSecurityDescriptorPartsA
 - LookupSecurityDescriptorPartsW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
---

# LookupSecurityDescriptorPartsA function


## -description


The <b>LookupSecurityDescriptorParts</b> function retrieves security information from a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">self-relative security descriptor</a>. 


## -parameters




### -param ppOwner [out, optional]

A pointer to a variable that receives a pointer to a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure. The function looks up the name associated with the owner 
<a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID)  in the <i>pSD</i> <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>, and returns a pointer to the name in the <b>ptstrName</b> member of the <b>TRUSTEE</b> structure. The function sets the <b>TrusteeForm</b> member to TRUSTEE_IS_NAME. 




This parameter can be <b>NULL</b> if you are not interested in the name of the owner.


### -param ppGroup [out, optional]

A pointer to a variable that receives a pointer to a <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure. The function looks up the name associated with the primary group SID of the security descriptor, and returns a pointer to the name in the <b>ptstrName</b> member of the <b>TRUSTEE</b> structure. The function sets the <b>TrusteeForm</b> member to TRUSTEE_IS_NAME.  




This parameter can be <b>NULL</b> if you are not interested in the name of the group.


### -param pcCountOfAccessEntries [out, optional]

A pointer to a <b>ULONG</b> that receives the number of 
<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structures returned in the <i>pListOfAccessEntries</i> array. This parameter can be <b>NULL</b> only if the <i>pListOfAccessEntries</i> parameter is also <b>NULL</b>.


### -param ppListOfAccessEntries [out, optional]

A pointer to a variable that receives a pointer to an array of <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structures that describe the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) in the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) of the security descriptor. The 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure in these <b>EXPLICIT_ACCESS</b> structures use the TRUSTEE_IS_NAME form. For a description of how an array of <b>EXPLICIT_ACCESS</b> structures describes the ACEs in an 
<a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL), see the 
<a href="https://msdn.microsoft.com/186aa6aa-efc3-4f8a-acad-e257da3dac0b">GetExplicitEntriesFromAcl</a> function. If this parameter is <b>NULL</b>, the <i>cCountOfAccessEntries</i> parameter must also be <b>NULL</b>.


### -param pcCountOfAuditEntries [out, optional]

A pointer to a <b>ULONG</b> that receives the number of <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structures returned in the <i>pListOfAuditEntries</i> array. This parameter can be <b>NULL</b> only if the <i>pListOfAuditEntries</i> parameter is also <b>NULL</b>.


### -param ppListOfAuditEntries [out, optional]

A pointer to a variable that receives a pointer to an array of <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structures that describe the ACEs in the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) of the security descriptor. The <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure in these <b>EXPLICIT_ACCESS</b> structures uses the TRUSTEE_IS_NAME form. If this parameter is <b>NULL</b>, the <i>cCountOfAuditEntries</i> parameter must also be <b>NULL</b>.


### -param pSD [in]

A pointer to an existing <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">self-relative security descriptor</a> from which the function retrieves security information.


## -returns



If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.




## -remarks



The <b>LookupSecurityDescriptorParts</b> function retrieves the names of the owner and primary group of the security descriptor. This function also returns descriptions of the ACEs in the DACL and audit-control entries in the SACL of the security descriptor.

The parameters other than <i>pSD</i> can be <b>NULL</b> if you are not interested in the information. If you do not want information about the DACL, both <i>pListOfAccessEntries</i> and <i>cCountOfAuditEntries</i> must be <b>NULL</b>. If you do not want information about the SACL, both <i>pListOfAuditEntries</i> and <i>cCountOfAuditEntries</i> must be <b>NULL</b>. Similarly, if you do want DACL or SACL information, both of the corresponding parameters must not be <b>NULL</b>.

When you have finished using any of the buffers returned by the <i>pOwner</i>, <i>pGroup</i>, <i>pListOfAccessEntries</i>, or <i>pListOfAuditEntries</i> parameters, free them by calling the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.

The <b>LookupSecurityDescriptorParts</b> function is intended for trusted servers that implement or expose security on their own objects. The function works with a self-relative security descriptor suitable for serializing into a stream and storing to disk, as a trusted server might require.




## -see-also




<a href="https://msdn.microsoft.com/980b8242-2ba2-469f-b834-da7d3fb22e14">ACE</a>



<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="authorization_functions.htm">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>



<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a>



<a href="https://msdn.microsoft.com/186aa6aa-efc3-4f8a-acad-e257da3dac0b">GetExplicitEntriesFromAcl</a>



<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>
 

 


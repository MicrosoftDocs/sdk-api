---
UID: NF:aclapi.BuildSecurityDescriptorA
title: BuildSecurityDescriptorA function
author: windows-sdk-content
description: Allocates and initializes a new security descriptor.
old-location: security\buildsecuritydescriptor.htm
old-project: secauthz
ms.assetid: becc1218-5bc3-4ab2-86f8-3ebd10e16966
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: BuildSecurityDescriptor, BuildSecurityDescriptor function [Security], BuildSecurityDescriptorA, BuildSecurityDescriptorW, _win32_buildsecuritydescriptor, aclapi/BuildSecurityDescriptor, aclapi/BuildSecurityDescriptorA, aclapi/BuildSecurityDescriptorW, security.buildsecuritydescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: BuildSecurityDescriptorW (Unicode) and BuildSecurityDescriptorA (ANSI)
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
 - API-MS-Win-security-trustee-l1-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-security-trustee-l1-1-1.dll
api_name:
 - BuildSecurityDescriptor
 - BuildSecurityDescriptorA
 - BuildSecurityDescriptorW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
---

# BuildSecurityDescriptorA function


## -description


The <b>BuildSecurityDescriptor</b> function allocates and initializes a new <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>. This function can initialize the new security descriptor by merging specified security information with the information in an existing security descriptor. If you do not specify an existing security descriptor, the function initializes a new security descriptor based on the specified security information.

The <b>BuildSecurityDescriptor</b> function creates a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">self-relative security descriptor</a>. The self-relative format makes the security descriptor suitable for storing in a stream.


## -parameters




### -param pOwner [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure that identifies the owner for the new security descriptor. If the structure uses the TRUSTEE_IS_NAME form, <b>BuildSecurityDescriptor</b> looks up the 
<a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) associated with the specified trustee name. 




If this parameter is <b>NULL</b>, the function uses the owner SID from the original security descriptor pointed to by <i>pOldSD</i>. If <i>pOldSD</i> is <b>NULL</b>, or if the owner SID in <i>pOldSD</i> is <b>NULL</b>, the owner SID is <b>NULL</b> in the new security descriptor.


### -param pGroup [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure that identifies the primary group SID for the new security descriptor. If the structure uses the TRUSTEE_IS_NAME form, <b>BuildSecurityDescriptor</b> looks up the SID associated with the specified trustee name. 




If this parameter is <b>NULL</b>, the function uses the group SID from the original security descriptor pointed to by <i>pOldSD</i>. If <i>pOldSD</i> is <b>NULL</b>, or if the group SID in <i>pOldSD</i> is <b>NULL</b>, the group SID is <b>NULL</b> in the new security descriptor.


### -param cCountOfAccessEntries [in]

The number of 
<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structures in the <i>pListOfAccessEntries</i> array.
					


### -param pListOfAccessEntries [in, optional]

A pointer to an array of <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structures that describe access control information for the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) of the new security descriptor. The function creates the new DACL by merging the information in the array with the DACL in <i>pOldSD</i>, if any. If <i>pOldSD</i> is <b>NULL</b>, or if the DACL in <i>pOldSD</i> is <b>NULL</b>, the function creates a new DACL based solely on the information in the array. For a description of the rules for creating an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a> from an array of <b>EXPLICIT_ACCESS</b> structures, see the 
<a href="https://msdn.microsoft.com/05960fc1-1ad2-4c19-a65c-62259af5e18c">SetEntriesInAcl</a> function. 




If <i>pListOfAccessEntries</i> is <b>NULL</b>, the new security descriptor gets the DACL from <i>pOldSD</i>. In this case, if <i>pOldSD</i> is <b>NULL</b>, or if the DACL in <i>pOldSD</i> is <b>NULL</b>, the new DACL is <b>NULL</b>.


### -param cCountOfAuditEntries [in]

The number of 
<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structures in the <i>pListOfAuditEntries</i> array.
					


### -param pListOfAuditEntries [in, optional]

A pointer to an array of <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structures that describe audit control information for the SACL of the new security descriptor. The function creates the new SACL by merging the information in the array with the SACL in <i>pOldSD</i>, if any. If <i>pOldSD</i> is <b>NULL</b>, or the SACL in <i>pOldSD</i> is <b>NULL</b>, the function creates a new SACL based solely on the information in the array. 




If <i>pListOfAuditEntries</i> is <b>NULL</b>, the new security descriptor gets the SACL from <i>pOldSD</i>. In this case, if <i>pOldSD</i> is <b>NULL</b>, or the SACL in <i>pOldSD</i> is <b>NULL</b>, the new SACL is <b>NULL</b>.


### -param pOldSD [in, optional]

A pointer to an existing self-relative 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure and its associated security information. The function builds the new security descriptor by merging the specified owner, group, access control, and audit-control information with the information in this security descriptor. This parameter can be <b>NULL</b>.


### -param pSizeNewSD [out]

A pointer to a variable that receives the size, in bytes, of the security descriptor.


### -param pNewSD [out]

A pointer to a variable that receives a pointer to the new security descriptor. The function allocates memory for the new security descriptor. You must call the 
<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function to free the returned buffer.


## -returns




						If the function succeeds, the function returns ERROR_SUCCESS.
						

If the function fails, it returns a nonzero error code defined in WinError.h.




## -remarks



The <b>BuildSecurityDescriptor</b> function is intended for trusted servers that implement or expose security on their own objects. The function uses self-relative security descriptors suitable for serializing into a stream and storing to disk, as a trusted server might require.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a>



<a href="https://msdn.microsoft.com/library/Aa373557(v=VS.85).aspx">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>



<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a>



<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>



<a href="https://msdn.microsoft.com/05960fc1-1ad2-4c19-a65c-62259af5e18c">SetEntriesInAcl</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>
 

 


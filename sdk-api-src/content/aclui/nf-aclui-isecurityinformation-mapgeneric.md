---
UID: NF:aclui.ISecurityInformation.MapGeneric
title: ISecurityInformation::MapGeneric
author: windows-sdk-content
description: The MapGeneric method requests that the generic access rights in an access mask be mapped to their corresponding standard and specific access rights.
old-location: security\isecurityinformation_mapgeneric.htm
tech.root: SecAuthZ
ms.assetid: 85ad4d42-11e7-4d26-943f-3d7451899c8e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISecurityInformation interface [Security],MapGeneric method, ISecurityInformation.MapGeneric, ISecurityInformation::MapGeneric, MapGeneric, MapGeneric method [Security], MapGeneric method [Security],ISecurityInformation interface, _win32_isecurityinformation_mapgeneric, aclui/ISecurityInformation::MapGeneric, security.isecurityinformation_mapgeneric
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: aclui.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Aclui.h
api_name:
 - ISecurityInformation.MapGeneric
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISecurityInformation::MapGeneric


## -description


The <b>MapGeneric</b> method requests that the generic access rights in an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a> be mapped to their corresponding standard and specific access rights. For more information about generic, standard, and specific access rights, see 
<a href="https://msdn.microsoft.com/da67c486-d2e7-4632-ac7a-c18aabc3f21d">Access Rights and Access Masks</a>.


## -parameters




### -param pguidObjectType [in]

A pointer to a 
<a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a> structure that identifies the type of object to which the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a> applies. If this member is <b>NULL</b> or a pointer to GUID_NULL, the access mask applies to the object itself.


### -param pAceFlags [in]

A pointer to the <b>AceFlags</b> member of the 
<a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a> structure from the ACE whose access mask is being mapped.


### -param pMask [in]

A pointer to an access mask that contains the generic access rights to map. Your implementation must map the generic access rights to the corresponding standard and specific access rights for the specified object type.


## -returns



If the function succeeds, the function returns S_OK.

 If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Your <b>MapGeneric</b> implementation can call the 
<a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a> function to map the generic access rights in the access mask.




## -see-also




<a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a>



<a href="https://msdn.microsoft.com/ca709f27-8463-4f11-92ac-2148796e640a">Access Control Editor</a>



<a href="authorization_functions.htm">Access Control Editor Functions</a>



<a href="https://msdn.microsoft.com/52cb20fd-7f3a-4984-a898-f4b9e9738e1a">CreateSecurityPage</a>



<a href="https://msdn.microsoft.com/756c94b0-946f-47eb-b4b4-db3e6e89fe46">EditSecurity</a>



<a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a>



<a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a>



<a href="https://msdn.microsoft.com/54b5cd73-4011-4dcf-a951-7350dbd6eeab">MapGenericMask</a>
 

 


---
UID: NF:aclui.ISecurityInformation.GetInheritTypes
title: ISecurityInformation::GetInheritTypes
author: windows-sdk-content
description: The GetInheritTypes method requests information about how ACEs can be inherited by child objects. For more information, see ACE Inheritance.
old-location: security\isecurityinformation_getinherittypes.htm
tech.root: secauthz
ms.assetid: dafe6c45-616f-4339-a119-9b88055b5d3a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetInheritTypes, GetInheritTypes method [Security], GetInheritTypes method [Security],ISecurityInformation interface, ISecurityInformation interface [Security],GetInheritTypes method, ISecurityInformation.GetInheritTypes, ISecurityInformation::GetInheritTypes, _win32_isecurityinformation_getinherittypes, aclui/ISecurityInformation::GetInheritTypes, security.isecurityinformation_getinherittypes
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
 - ISecurityInformation.GetInheritTypes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISecurityInformation::GetInheritTypes


## -description


The <b>GetInheritTypes</b> method requests information about how ACEs can be inherited by child objects. For more information, see 
<a href="https://msdn.microsoft.com/a9e5ad4d-61c6-43ed-a162-460683bcdb16">ACE Inheritance</a>.


## -parameters




### -param ppInheritTypes [out]

A pointer to a variable you should set to a pointer to an array of 
<a href="https://msdn.microsoft.com/e8382c14-d3b4-4a7e-aeaa-06ef44d6ace2">SI_INHERIT_TYPE</a> structures. The array should include one entry for each combination of inheritance flags and child object type that you support.


### -param pcInheritTypes [out]

A pointer to a variable that you should set to indicate the number of entries in the <i>ppInheritTypes</i> array.


## -returns



Returns S_OK if successful.

Returns a nonzero error code if an error occurs.




## -remarks



The access control editor does not free the pointer returned in <i>ppInheritTypes</i>.




## -see-also




<a href="https://msdn.microsoft.com/ca709f27-8463-4f11-92ac-2148796e640a">Access Control Editor</a>



<a href="authorization_functions.htm">Access Control Editor Functions</a>



<a href="https://msdn.microsoft.com/52cb20fd-7f3a-4984-a898-f4b9e9738e1a">CreateSecurityPage</a>



<a href="https://msdn.microsoft.com/756c94b0-946f-47eb-b4b4-db3e6e89fe46">EditSecurity</a>



<a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a>



<a href="https://msdn.microsoft.com/e8382c14-d3b4-4a7e-aeaa-06ef44d6ace2">SI_INHERIT_TYPE</a>
 

 


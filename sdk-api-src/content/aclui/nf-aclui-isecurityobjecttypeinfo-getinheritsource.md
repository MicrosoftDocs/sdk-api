---
UID: NF:aclui.ISecurityObjectTypeInfo.GetInheritSource
title: ISecurityObjectTypeInfo::GetInheritSource
author: windows-sdk-content
description: The ISecurityObjectTypeInfo::GetInheritSource method provides a means of determining the source of inherited access control entries in discretionary access control lists and system access control lists.
old-location: security\isecurityobjecttypeinfo_getinheritsource.htm
tech.root: secauthz
ms.assetid: e058ca98-08dc-4a3f-9521-adcc5990eae7
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: GetInheritSource, GetInheritSource method [Security], GetInheritSource method [Security],ISecurityObjectTypeInfo interface, ISecurityObjectTypeInfo interface [Security],GetInheritSource method, ISecurityObjectTypeInfo.GetInheritSource, ISecurityObjectTypeInfo::GetInheritSource, aclui/ISecurityObjectTypeInfo::GetInheritSource, security.isecurityobjecttypeinfo_getinheritsource
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
 - ISecurityObjectTypeInfo.GetInheritSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISecurityObjectTypeInfo::GetInheritSource


## -description


The <b>GetInheritSource</b> method provides a means of determining the source of inherited <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) in <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control lists</a> (DACLs) and <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control lists</a> (SACLs).


## -parameters




### -param si [in]

A <a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> structure that represents the security information of the object.


### -param pACL [in]

A pointer to an <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> structure that represents the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL) of the object.


### -param ppInheritArray [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6839f67a-6c72-406d-b55e-bc366aaad107">INHERITED_FROM</a> structure that receives an array of <b>INHERITED_FROM</b> structures. The length of this array is the same as the number of <a href="https://msdn.microsoft.com/980b8242-2ba2-469f-b834-da7d3fb22e14">ACEs</a> in the ACL referenced by <i>pACL</i>. Each <b>INHERITED_FROM</b> entry in <i>ppInheritArray</i> provides inheritance information for the corresponding <b>ACE</b> entry in <i>pACL</i>.


## -returns



If the function is successful, the return value is S_OK.

 
If the function fails, the return value is an <b>HRESULT</b> that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




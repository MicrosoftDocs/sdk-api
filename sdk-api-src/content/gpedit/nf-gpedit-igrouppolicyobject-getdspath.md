---
UID: NF:gpedit.IGroupPolicyObject.GetDSPath
title: IGroupPolicyObject::GetDSPath method
author: windows-driver-content
description: The GetDSPath method retrieves the Active Directory path to the root of the specified GPO section.
old-location: policy\igrouppolicyobject_getdspath.htm
old-project: Policy
ms.assetid: 0d6d0b3d-5ad4-4363-a123-f074193b75e2
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GPO_SECTION_MACHINE, GPO_SECTION_ROOT, GPO_SECTION_USER, GetDSPath method [Group Policy], GetDSPath method [Group Policy], IGroupPolicyObject interface, GetDSPath,IGroupPolicyObject.GetDSPath, IGroupPolicyObject, IGroupPolicyObject interface [Group Policy], GetDSPath method, IGroupPolicyObject::GetDSPath, _win32_igrouppolicyobject_getdspath, gpedit/IGroupPolicyObject::GetDSPath, policy.igrouppolicyobject_getdspath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpedit.dll
api_name:
-	IGroupPolicyObject.GetDSPath
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGroupPolicyObject::GetDSPath method


## -description


The
    <b>GetDSPath</b> method retrieves the Active Directory path to the root of the specified GPO section.


## -parameters




### -param dwSection [in]

Specifies the GPO section. This parameter can be one of the following values.



#### GPO_SECTION_ROOT

Root section



#### GPO_SECTION_USER

User section



#### GPO_SECTION_MACHINE

Computer section


### -param pszPath [out]

Pointer to a buffer that receives the path, in ADSI format (LDAP://cn=<i>user</i>, ou=<i>users</i>, dc=<i>coname</i>, dc=<i>com</i>).


### -param cchMaxPath [in]

Specifies the maximum number of characters that can be stored in the <i>pszPath</i> buffer.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



If you call the 
<b>GetDSPath</b> method and specify a computer GPO, the method succeeds, but on return, the <i>pszPath</i> parameter contains an empty string. This is because computer GPOs do not have Active Directory storage; they have only file system storage.

To retrieve the file system path to the root of a GPO section, you can call the 
<a href="https://msdn.microsoft.com/9f0837ff-31bb-4eaa-82e4-ef127f8e605a">GetFileSysPath</a> method.




## -see-also




<a href="https://msdn.microsoft.com/9f0837ff-31bb-4eaa-82e4-ef127f8e605a">GetFileSysPath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt432961">GetPath</a>



<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a>
 

 


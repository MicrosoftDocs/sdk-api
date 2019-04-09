---
UID: NF:gpedit.IGroupPolicyObject.GetFileSysPath
title: IGroupPolicyObject::GetFileSysPath (gpedit.h)
author: windows-sdk-content
description: The GetFileSysPath method retrieves the file system path to the root of the specified GPO section. The path is in UNC format.
old-location: policy\igrouppolicyobject_getfilesyspath.htm
tech.root: Policy
ms.assetid: 9f0837ff-31bb-4eaa-82e4-ef127f8e605a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPO_SECTION_MACHINE, GPO_SECTION_ROOT, GPO_SECTION_USER, GetFileSysPath, GetFileSysPath method [Group Policy], GetFileSysPath method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],GetFileSysPath method, IGroupPolicyObject.GetFileSysPath, IGroupPolicyObject::GetFileSysPath, _win32_igrouppolicyobject_getfilesyspath, gpedit/IGroupPolicyObject::GetFileSysPath, policy.igrouppolicyobject_getfilesyspath
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
req.lib: 
req.dll: Gpedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGroupPolicyObject.GetFileSysPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGroupPolicyObject::GetFileSysPath


## -description


The
    <b>GetFileSysPath</b> method retrieves the file system path to the root of the specified GPO section. The path is in UNC format.


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

Pointer to a buffer that receives the path.


### -param cchMaxPath [in]

Specifies the maximum number of characters that can be stored in the <i>pszPath</i> buffer.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



To retrieve the Active Directory path to the root of a GPO section, you can call the 
<a href="https://msdn.microsoft.com/0d6d0b3d-5ad4-4363-a123-f074193b75e2">GetDSPath</a> method.




## -see-also




<a href="https://msdn.microsoft.com/0d6d0b3d-5ad4-4363-a123-f074193b75e2">GetDSPath</a>



<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a>
 

 


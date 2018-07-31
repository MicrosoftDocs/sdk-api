---
UID: NS:winnt._ACL
title: "_ACL"
author: windows-sdk-content
description: Header of an access control list (ACL).
old-location: security\acl.htm
old-project: SecAuthZ
ms.assetid: 0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PACL, ACL, ACL structure [Security], PACL, PACL structure pointer [Security], _ACL, _win32_acl_str, security.acl, winnt/ACL, winnt/PACL"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
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
req.typenames: ACL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - ACL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _ACL structure


## -description


The <b>ACL</b> structure is the header of an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL). A complete ACL consists of an <b>ACL</b> structure followed by an ordered list of zero or more  <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs).


## -struct-fields




### -field AclRevision

Specifies the revision level of the ACL. This value should be ACL_REVISION, unless the ACL contains an object-specific ACE, in which case this value must be ACL_REVISION_DS. All ACEs in an ACL must be at the same revision level.


### -field Sbz1

Specifies a zero byte of <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">padding</a> that aligns the <b>AclRevision</b> member on a 16-bit boundary.


### -field AclSize

Specifies the size, in bytes, of the ACL. This value includes both the <b>ACL</b> structure and all the ACEs.


### -field AceCount

Specifies the number of ACEs stored in the ACL.


### -field Sbz2

Specifies two zero-bytes of <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">padding</a> that align the <b>ACL</b> structure on a 32-bit boundary.


## -remarks



An ACL includes a sequential list of zero or more ACEs. The individual ACEs in an ACL are numbered from 0 to <i>n</i>, where <i>n</i>+1 is the number of ACEs in the ACL. When editing an ACL, an application refers to an ACE within the ACL by the ACE's index.

There are two types of ACL: discretionary and system.

A <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) is controlled by the owner of an object or anyone granted WRITE_DAC access to the object. It specifies the access particular users and groups can have to an object. For example, the owner of a file can use a DACL to control which users and groups can and cannot have access to the file.

An object can also have system-level security information associated with it, in the form of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) controlled by a system administrator. A SACL  allows the system administrator to audit any attempts to gain access to an object.

For a list of currently defined ACE structures, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff538844">ACE</a>.

A fourth ACE structure, <a href="https://msdn.microsoft.com/library/windows/hardware/ff556769">SYSTEM_ALARM_ACE</a>, is not currently supported.

The <b>ACL</b> structure is to be treated as though it were opaque and applications are not to attempt to work with its members directly. To ensure that ACLs are semantically correct, applications can use the functions listed in the See Also section to create and manipulate ACLs.

Each <b>ACL</b> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff538844">ACE</a> structure begins on a <b>DWORD</b> boundary.

The maximum size for an ACL, including its ACEs, is 64 KB.




## -see-also




<a href="https://msdn.microsoft.com/f472d864-a273-49b5-b5e2-98772989971e">AddAce</a>



<a href="https://msdn.microsoft.com/02ce45ad-3d51-4548-848e-a62bf4bf72a8">DeleteAce</a>



<a href="https://msdn.microsoft.com/23ef6abd-03e9-439e-ba05-629c8d61cd66">GetAclInformation</a>



<a href="https://msdn.microsoft.com/8006c8bb-4976-463f-b074-a59c3bbab36b">GetSecurityDescriptorDacl</a>



<a href="https://msdn.microsoft.com/6bf59735-aaa3-4751-8c98-00cc197df4e5">GetSecurityDescriptorSacl</a>



<a href="https://msdn.microsoft.com/b990a7bd-7840-4c10-baf8-68b3862147f4">InitializeAcl</a>



<a href="https://msdn.microsoft.com/3ae9f147-4e90-44df-a1af-cf6ebad92aea">IsValidAcl</a>



<a href="https://msdn.microsoft.com/bb4dd7f9-2f15-4a27-89c9-1675f4fb8d92">SetAclInformation</a>



<a href="https://msdn.microsoft.com/a873b803-391e-47e1-af7e-6dad7195968c">SetSecurityDescriptorDacl</a>



<a href="https://msdn.microsoft.com/21615b63-0619-4c0c-a1b8-88ed09a1235c">SetSecurityDescriptorSacl</a>
 

 


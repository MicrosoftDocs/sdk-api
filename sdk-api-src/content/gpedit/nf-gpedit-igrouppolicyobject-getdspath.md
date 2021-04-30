---
UID: NF:gpedit.IGroupPolicyObject.GetDSPath
title: IGroupPolicyObject::GetDSPath (gpedit.h)
description: The GetDSPath method retrieves the Active Directory path to the root of the specified GPO section.
helpviewer_keywords: ["GPO_SECTION_MACHINE","GPO_SECTION_ROOT","GPO_SECTION_USER","GetDSPath","GetDSPath method [Group Policy]","GetDSPath method [Group Policy]","IGroupPolicyObject interface","IGroupPolicyObject interface [Group Policy]","GetDSPath method","IGroupPolicyObject.GetDSPath","IGroupPolicyObject::GetDSPath","_win32_igrouppolicyobject_getdspath","gpedit/IGroupPolicyObject::GetDSPath","policy.igrouppolicyobject_getdspath"]
old-location: policy\igrouppolicyobject_getdspath.htm
tech.root: Policy
ms.assetid: 0d6d0b3d-5ad4-4363-a123-f074193b75e2
ms.date: 12/05/2018
ms.keywords: GPO_SECTION_MACHINE, GPO_SECTION_ROOT, GPO_SECTION_USER, GetDSPath, GetDSPath method [Group Policy], GetDSPath method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],GetDSPath method, IGroupPolicyObject.GetDSPath, IGroupPolicyObject::GetDSPath, _win32_igrouppolicyobject_getdspath, gpedit/IGroupPolicyObject::GetDSPath, policy.igrouppolicyobject_getdspath
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGroupPolicyObject::GetDSPath
 - gpedit/IGroupPolicyObject::GetDSPath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGroupPolicyObject.GetDSPath
---

# IGroupPolicyObject::GetDSPath


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
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getfilesyspath">GetFileSysPath</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getfilesyspath">GetFileSysPath</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getpath">GetPath</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a>
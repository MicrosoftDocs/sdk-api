---
UID: NF:gpedit.IRSOPInformation.GetNamespace
title: IRSOPInformation::GetNamespace (gpedit.h)
description: The GetNameSpace method retrieves the namespace from which the RSoP data is being displayed.
helpviewer_keywords: ["GPO_SECTION_MACHINE","GPO_SECTION_ROOT","GPO_SECTION_USER","GetNameSpace method [Group Policy]","GetNameSpace method [Group Policy]","IRSOPInformation interface","GetNamespace","IRSOPInformation interface [Group Policy]","GetNameSpace method","IRSOPInformation.GetNamespace","IRSOPInformation::GetNameSpace","IRSOPInformation::GetNamespace","_win32_irsopinformation_getnamespace","gpedit/IRSOPInformation::GetNameSpace","policy.irsopinformation_getnamespace"]
old-location: policy\irsopinformation_getnamespace.htm
tech.root: Policy
ms.assetid: 3575072c-88d7-482c-bc8b-dca9f6d68577
ms.date: 12/05/2018
ms.keywords: GPO_SECTION_MACHINE, GPO_SECTION_ROOT, GPO_SECTION_USER, GetNameSpace method [Group Policy], GetNameSpace method [Group Policy],IRSOPInformation interface, GetNamespace, IRSOPInformation interface [Group Policy],GetNameSpace method, IRSOPInformation.GetNamespace, IRSOPInformation::GetNameSpace, IRSOPInformation::GetNamespace, _win32_irsopinformation_getnamespace, gpedit/IRSOPInformation::GetNameSpace, policy.irsopinformation_getnamespace
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
 - IRSOPInformation::GetNamespace
 - gpedit/IRSOPInformation::GetNamespace
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
 - IRSOPInformation.GetNameSpace
---

# IRSOPInformation::GetNamespace


## -description

The
    <b>GetNameSpace</b> method retrieves the namespace from which the RSoP data is being displayed.

## -parameters

### -param dwSection [in]

Specifies the GPO section. This parameter can be one of the following values.



#### GPO_SECTION_ROOT

Root section



#### GPO_SECTION_USER

User section



#### GPO_SECTION_MACHINE

Computer section

### -param pszName [out]

Receives the namespace from which the RSoP data is being displayed. The computer and user RSoP data are in sub-namespaces under this namespace. Computer RSoP data is under the Computer sub-namespace, and user RSoP data is under the User sub-namespace.

### -param cchMaxLength [in]

Specifies the size, in characters, of the <i>pszName</i> buffer.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-irsopinformation">IRSOPInformation</a>
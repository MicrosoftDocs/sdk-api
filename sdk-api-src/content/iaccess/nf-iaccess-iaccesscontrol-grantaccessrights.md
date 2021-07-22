---
UID: NF:iaccess.IAccessControl.GrantAccessRights
title: IAccessControl::GrantAccessRights (iaccess.h)
description: Merges the new list of access rights with the existing access rights on the object.
helpviewer_keywords: ["GrantAccessRights","GrantAccessRights method [COM]","GrantAccessRights method [COM]","IAccessControl interface","IAccessControl interface [COM]","GrantAccessRights method","IAccessControl.GrantAccessRights","IAccessControl::GrantAccessRights","_com_iaccesscontrol_grantaccessrights","com.iaccesscontrol_grantaccessrights","iaccess/IAccessControl::GrantAccessRights"]
old-location: com\iaccesscontrol_grantaccessrights.htm
tech.root: com
ms.assetid: f8ec6743-633b-4c79-afac-68eb20e07b2a
ms.date: 12/05/2018
ms.keywords: GrantAccessRights, GrantAccessRights method [COM], GrantAccessRights method [COM],IAccessControl interface, IAccessControl interface [COM],GrantAccessRights method, IAccessControl.GrantAccessRights, IAccessControl::GrantAccessRights, _com_iaccesscontrol_grantaccessrights, com.iaccesscontrol_grantaccessrights, iaccess/IAccessControl::GrantAccessRights
req.header: iaccess.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: IAccess.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAccessControl::GrantAccessRights
 - iaccess/IAccessControl::GrantAccessRights
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - IAccess.h
api_name:
 - IAccessControl.GrantAccessRights
---

# IAccessControl::GrantAccessRights


## -description

Merges the new list of access rights with the existing access rights on the object.

## -parameters

### -param pAccessList [in]

A pointer to the [ACTRL_ACCESS](../accctrl/ns-accctrl-explicit_access_a.md) structure that contains an array of access lists for the object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Merging the new access rights list with the existing access rights ensures that the object will have at least the indicated access rights. This merge process consists of adding the new denied access rights before the old denied access rights, and the new allowed access rights before the existing allowed rights. None of the existing rights are removed.

Following a merge, the access rights on an object are ordered as follows:

<ol>
<li>[New Access Denied]</li>
<li>[Old Access Denied]</li>
<li>[New Access Allowed]</li>
<li>[Old Access Allowed]</li>
</ol>
The system-supplied implementation of [ACTRL_ACCESS](../accctrl/ns-accctrl-explicit_access_a.md) structure be set to 1. In addition, the <b>lpProperty</b> member of the <a href="/windows/desktop/api/accctrl/ns-accctrl-actrl_property_entrya">ACTRL_PROPERTY_ENTRYW</a> structure must be <b>NULL</b> to indicate that the access entry list applies to the object itself.

## -see-also

<a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>
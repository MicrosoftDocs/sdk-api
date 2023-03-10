---
UID: NF:iaccess.IAccessControl.RevokeAccessRights
title: IAccessControl::RevokeAccessRights (iaccess.h)
description: Removes any explicit entries for the list of trustees.
helpviewer_keywords: ["IAccessControl interface [COM]","RevokeAccessRights method","IAccessControl.RevokeAccessRights","IAccessControl::RevokeAccessRights","RevokeAccessRights","RevokeAccessRights method [COM]","RevokeAccessRights method [COM]","IAccessControl interface","_com_iaccesscontrol_revokeaccessrights","com.iaccesscontrol_revokeaccessrights","iaccess/IAccessControl::RevokeAccessRights"]
old-location: com\iaccesscontrol_revokeaccessrights.htm
tech.root: com
ms.assetid: 09b37002-0ad3-43c2-8a39-b440158310bb
ms.date: 12/05/2018
ms.keywords: IAccessControl interface [COM],RevokeAccessRights method, IAccessControl.RevokeAccessRights, IAccessControl::RevokeAccessRights, RevokeAccessRights, RevokeAccessRights method [COM], RevokeAccessRights method [COM],IAccessControl interface, _com_iaccesscontrol_revokeaccessrights, com.iaccesscontrol_revokeaccessrights, iaccess/IAccessControl::RevokeAccessRights
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
 - IAccessControl::RevokeAccessRights
 - iaccess/IAccessControl::RevokeAccessRights
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
 - IAccessControl.RevokeAccessRights
---

# IAccessControl::RevokeAccessRights


## -description

Removes any explicit entries for the list of trustees.

## -parameters

### -param lpProperty [in]

The name of the property. If you are using the COM implementation of <a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>, this parameter must be <b>NULL</b>.

### -param cTrustees [in]

The number of trustees in the list. This parameter cannot be 0.

### -param prgTrustees [in]

A pointer to an array of trustee names. See <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Even after removing explicit entries, the trustees might still have access entries due to group inclusion.

## -see-also

<a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>
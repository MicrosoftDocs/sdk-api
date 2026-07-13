---
UID: NF:iaccess.IAccessControl.SetOwner
title: IAccessControl::SetOwner (iaccess.h)
description: Sets the owner or the group of an item.
helpviewer_keywords: ["IAccessControl interface [COM]","SetOwner method","IAccessControl.SetOwner","IAccessControl::SetOwner","SetOwner","SetOwner method [COM]","SetOwner method [COM]","IAccessControl interface","_com_iaccesscontrol_setowner","com.iaccesscontrol_setowner","iaccess/IAccessControl::SetOwner"]
old-location: com\iaccesscontrol_setowner.htm
tech.root: com
ms.assetid: 92406043-f4a4-43e4-9b17-087066823ce4
ms.date: 12/05/2018
ms.keywords: IAccessControl interface [COM],SetOwner method, IAccessControl.SetOwner, IAccessControl::SetOwner, SetOwner, SetOwner method [COM], SetOwner method [COM],IAccessControl interface, _com_iaccesscontrol_setowner, com.iaccesscontrol_setowner, iaccess/IAccessControl::SetOwner
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
 - IAccessControl::SetOwner
 - iaccess/IAccessControl::SetOwner
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
 - IAccessControl.SetOwner
---

# IAccessControl::SetOwner


## -description

Sets the owner or the group of an item.

## -parameters

### -param pOwner [in]

The address of the <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure for the owner.

### -param pGroup [in]

The address of the <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure for the group.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>SetOwner</b> method is not implemented by CLSID_DCOMAccessControl.

## -see-also

<a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>
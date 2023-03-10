---
UID: NF:shobjidl_core.IApplicationAssociationRegistration.ClearUserAssociations
title: IApplicationAssociationRegistration::ClearUserAssociations (shobjidl_core.h)
description: Removes all per-user associations for the current user. This results in a reversion to machine defaults, if they exist. Not intended for use in Windows 8.
helpviewer_keywords: ["ClearUserAssociations","ClearUserAssociations method [Windows Shell]","ClearUserAssociations method [Windows Shell]","IApplicationAssociationRegistration interface","IApplicationAssociationRegistration interface [Windows Shell]","ClearUserAssociations method","IApplicationAssociationRegistration.ClearUserAssociations","IApplicationAssociationRegistration::ClearUserAssociations","_shell_IApplicationAssociationRegistration_ClearUserAssociations","shell.IApplicationAssociationRegistration_ClearUserAssociations","shobjidl_core/IApplicationAssociationRegistration::ClearUserAssociations"]
old-location: shell\IApplicationAssociationRegistration_ClearUserAssociations.htm
tech.root: shell
ms.assetid: dcc0990a-f678-47bb-9462-905940ac87d6
ms.date: 12/05/2018
ms.keywords: ClearUserAssociations, ClearUserAssociations method [Windows Shell], ClearUserAssociations method [Windows Shell],IApplicationAssociationRegistration interface, IApplicationAssociationRegistration interface [Windows Shell],ClearUserAssociations method, IApplicationAssociationRegistration.ClearUserAssociations, IApplicationAssociationRegistration::ClearUserAssociations, _shell_IApplicationAssociationRegistration_ClearUserAssociations, shell.IApplicationAssociationRegistration_ClearUserAssociations, shobjidl_core/IApplicationAssociationRegistration::ClearUserAssociations
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IApplicationAssociationRegistration::ClearUserAssociations
 - shobjidl_core/IApplicationAssociationRegistration::ClearUserAssociations
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IApplicationAssociationRegistration.ClearUserAssociations
---

# IApplicationAssociationRegistration::ClearUserAssociations


## -description

Removes all per-user associations for the current user. This results in a reversion to machine defaults, if they exist. Not intended for use in Windows 8.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/shell/default-programs">Default Programs</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration">IApplicationAssociationRegistration</a>

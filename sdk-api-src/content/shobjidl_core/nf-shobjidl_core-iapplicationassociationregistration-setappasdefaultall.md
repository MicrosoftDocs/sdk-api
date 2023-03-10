---
UID: NF:shobjidl_core.IApplicationAssociationRegistration.SetAppAsDefaultAll
title: IApplicationAssociationRegistration::SetAppAsDefaultAll (shobjidl_core.h)
description: Sets an application as the default for all of the registered associations of any type for that application. Not intended for use in Windows 8.
helpviewer_keywords: ["IApplicationAssociationRegistration interface [Windows Shell]","SetAppAsDefaultAll method","IApplicationAssociationRegistration.SetAppAsDefaultAll","IApplicationAssociationRegistration::SetAppAsDefaultAll","SetAppAsDefaultAll","SetAppAsDefaultAll method [Windows Shell]","SetAppAsDefaultAll method [Windows Shell]","IApplicationAssociationRegistration interface","_shell_IApplicationAssociationRegistration_SetAppAsDefaultAll","shell.IApplicationAssociationRegistration_SetAppAsDefaultAll","shobjidl_core/IApplicationAssociationRegistration::SetAppAsDefaultAll"]
old-location: shell\IApplicationAssociationRegistration_SetAppAsDefaultAll.htm
tech.root: shell
ms.assetid: 3e9ad8ba-0f0e-46e6-ab0b-61c35bfd2dc6
ms.date: 12/05/2018
ms.keywords: IApplicationAssociationRegistration interface [Windows Shell],SetAppAsDefaultAll method, IApplicationAssociationRegistration.SetAppAsDefaultAll, IApplicationAssociationRegistration::SetAppAsDefaultAll, SetAppAsDefaultAll, SetAppAsDefaultAll method [Windows Shell], SetAppAsDefaultAll method [Windows Shell],IApplicationAssociationRegistration interface, _shell_IApplicationAssociationRegistration_SetAppAsDefaultAll, shell.IApplicationAssociationRegistration_SetAppAsDefaultAll, shobjidl_core/IApplicationAssociationRegistration::SetAppAsDefaultAll
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
 - IApplicationAssociationRegistration::SetAppAsDefaultAll
 - shobjidl_core/IApplicationAssociationRegistration::SetAppAsDefaultAll
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
 - IApplicationAssociationRegistration.SetAppAsDefaultAll
---

# IApplicationAssociationRegistration::SetAppAsDefaultAll


## -description

Sets an application as the default for all of the registered associations of any <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype">type</a> for that application. Not intended for use in Windows 8.

## -parameters

### -param pszAppRegistryName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated Unicode string that specifies the registered name of the application.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/shell/default-programs">Default Programs</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration">IApplicationAssociationRegistration</a>
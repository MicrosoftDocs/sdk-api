---
UID: NF:shobjidl.IApplicationAssociationRegistrationUI.LaunchAdvancedAssociationUI
title: IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI (shobjidl.h)
description: Launches an advanced association dialog box through which the user can customize the associations for the application specified in pszAppRegName.
helpviewer_keywords: ["IApplicationAssociationRegistrationUI interface [Windows Shell]","LaunchAdvancedAssociationUI method","IApplicationAssociationRegistrationUI.LaunchAdvancedAssociationUI","IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI","LaunchAdvancedAssociationUI","LaunchAdvancedAssociationUI method [Windows Shell]","LaunchAdvancedAssociationUI method [Windows Shell]","IApplicationAssociationRegistrationUI interface","_shell_IApplicationAssociationRegistrationUI_LaunchAdvancedAssociationUI","shell.IApplicationAssociationRegistrationUI_LaunchAdvancedAssociationUI","shobjidl/IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI"]
old-location: shell\IApplicationAssociationRegistrationUI_LaunchAdvancedAssociationUI.htm
tech.root: shell
ms.assetid: db2fc087-2f22-40df-8ec9-f673c0fe81ff
ms.date: 12/05/2018
ms.keywords: IApplicationAssociationRegistrationUI interface [Windows Shell],LaunchAdvancedAssociationUI method, IApplicationAssociationRegistrationUI.LaunchAdvancedAssociationUI, IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI, LaunchAdvancedAssociationUI, LaunchAdvancedAssociationUI method [Windows Shell], LaunchAdvancedAssociationUI method [Windows Shell],IApplicationAssociationRegistrationUI interface, _shell_IApplicationAssociationRegistrationUI_LaunchAdvancedAssociationUI, shell.IApplicationAssociationRegistrationUI_LaunchAdvancedAssociationUI, shobjidl/IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI
req.header: shobjidl.h
req.include-header: 
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
 - IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI
 - shobjidl/IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IApplicationAssociationRegistrationUI.LaunchAdvancedAssociationUI
---

# IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI


## -description

Launches an advanced association dialog box through which the user can customize the associations for the application specified in <i>pszAppRegName</i>.

## -parameters

### -param pszAppRegistryName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated Unicode string that specifies the registered name of the application. This value is only valid if it matches one of the application strings registered under <b>HKCU\Software\RegisteredApplications</b> or under <b>HKLM\Software\RegisteredApplications</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Starting in Windows 10, this does not launch the association dialog box. It displays a dialog to the user informing them that they can change the default programs used to open file extensions in their <b>Settings</b>

## -see-also

<a href="/windows/desktop/shell/default-programs">Default Programs</a>



<a href="/windows/desktop/api/shobjidl/nn-shobjidl-iapplicationassociationregistrationui">IApplicationAssociationRegistrationUI</a>
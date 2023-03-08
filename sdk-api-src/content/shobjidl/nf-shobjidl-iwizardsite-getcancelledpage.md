---
UID: NF:shobjidl.IWizardSite.GetCancelledPage
title: IWizardSite::GetCancelledPage (shobjidl.h)
description: Called when the user cancels navigation through the wizard extension. Gets the handle of the PROPSHEETPAGE that represents the wizard page to display when the user cancels navigation while in the wizard extension.
helpviewer_keywords: ["GetCancelledPage","GetCancelledPage method [Windows Shell]","GetCancelledPage method [Windows Shell]","IWizardSite interface","IWizardSite interface [Windows Shell]","GetCancelledPage method","IWizardSite.GetCancelledPage","IWizardSite::GetCancelledPage","_shell_IWizardSite_GetCancelledPage","shell.IWizardSite_GetCancelledPage","shobjidl/IWizardSite::GetCancelledPage"]
old-location: shell\IWizardSite_GetCancelledPage.htm
tech.root: shell
ms.assetid: 682f5624-5fec-4bc9-9455-150e8e951538
ms.date: 12/05/2018
ms.keywords: GetCancelledPage, GetCancelledPage method [Windows Shell], GetCancelledPage method [Windows Shell],IWizardSite interface, IWizardSite interface [Windows Shell],GetCancelledPage method, IWizardSite.GetCancelledPage, IWizardSite::GetCancelledPage, _shell_IWizardSite_GetCancelledPage, shell.IWizardSite_GetCancelledPage, shobjidl/IWizardSite::GetCancelledPage
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWizardSite::GetCancelledPage
 - shobjidl/IWizardSite::GetCancelledPage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IWizardSite.GetCancelledPage
---

# IWizardSite::GetCancelledPage


## -description

Called when the user cancels navigation through the wizard extension. Gets the handle of the <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> that represents the wizard page to display when the user cancels navigation while in the wizard extension.

## -parameters

### -param phpage [out]

Type: <b>HPROPSHEETPAGE*</b>

A pointer to a handle variable of type <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> that receives the wizard page to display when the user cancels navigation while in the wizard extension.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
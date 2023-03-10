---
UID: NF:shobjidl.IWizardSite.GetPreviousPage
title: IWizardSite::GetPreviousPage (shobjidl.h)
description: Called when the user navigates backward out of the wizard extension. Gets the handle of the PROPSHEETPAGE that represents the wizard page that is before the wizard extension page.
helpviewer_keywords: ["GetPreviousPage","GetPreviousPage method [Windows Shell]","GetPreviousPage method [Windows Shell]","IWizardSite interface","IWizardSite interface [Windows Shell]","GetPreviousPage method","IWizardSite.GetPreviousPage","IWizardSite::GetPreviousPage","_shell_IWizardSite_GetPreviousPage","shell.IWizardSite_GetPreviousPage","shobjidl/IWizardSite::GetPreviousPage"]
old-location: shell\IWizardSite_GetPreviousPage.htm
tech.root: shell
ms.assetid: 998eabc5-a0d4-450f-92bf-cf81f74c48d2
ms.date: 12/05/2018
ms.keywords: GetPreviousPage, GetPreviousPage method [Windows Shell], GetPreviousPage method [Windows Shell],IWizardSite interface, IWizardSite interface [Windows Shell],GetPreviousPage method, IWizardSite.GetPreviousPage, IWizardSite::GetPreviousPage, _shell_IWizardSite_GetPreviousPage, shell.IWizardSite_GetPreviousPage, shobjidl/IWizardSite::GetPreviousPage
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
 - IWizardSite::GetPreviousPage
 - shobjidl/IWizardSite::GetPreviousPage
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
 - IWizardSite.GetPreviousPage
---

# IWizardSite::GetPreviousPage


## -description

Called when the user navigates backward out of the wizard extension. Gets the handle of the <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> that represents the wizard page that is before the wizard extension page.

## -parameters

### -param phpage [out]

Type: <b>HPROPSHEETPAGE*</b>

A pointer to a variable handle of type <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> that represents the wizard page that comes immediately before the wizard extension page.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
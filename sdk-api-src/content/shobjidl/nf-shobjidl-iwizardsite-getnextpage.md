---
UID: NF:shobjidl.IWizardSite.GetNextPage
title: IWizardSite::GetNextPage
author: windows-sdk-content
description: Called when the user navigates forward past the wizard extension pages. Gets the handle of the PROPSHEETPAGE that represents the wizard page immediately following the wizard extension page.
old-location: shell\IWizardSite_GetNextPage.htm
tech.root: shell
ms.assetid: 61f9b288-40d0-4e36-84e7-6b7bd5d3f5f1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetNextPage, GetNextPage method [Windows Shell], GetNextPage method [Windows Shell],IWizardSite interface, IWizardSite interface [Windows Shell],GetNextPage method, IWizardSite.GetNextPage, IWizardSite::GetNextPage, _shell_IWizardSite_GetNextPage, shell.IWizardSite_GetNextPage, shobjidl/IWizardSite::GetNextPage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IWizardSite.GetNextPage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl.h
: 
- IWizardSite.GetNextPage
: 
---

# IWizardSite::GetNextPage


## -description


Called when the user navigates forward past the wizard extension pages. Gets the handle of the <a href="https://msdn.microsoft.com/69ceb9f4-f68c-4c60-9610-4c1977aae4b8">PROPSHEETPAGE</a> that represents the wizard page immediately following the wizard extension page.


## -parameters




### -param phpage [out]

Type: <b>HPROPSHEETPAGE*</b>

A pointer to a handle variable of type <a href="https://msdn.microsoft.com/69ceb9f4-f68c-4c60-9610-4c1977aae4b8">PROPSHEETPAGE</a> for the wizard page following the extension page.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




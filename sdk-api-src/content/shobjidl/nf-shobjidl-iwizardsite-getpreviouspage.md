---
UID: NF:shobjidl.IWizardSite.GetPreviousPage
title: IWizardSite::GetPreviousPage
author: windows-sdk-content
description: Called when the user navigates backward out of the wizard extension. Gets the handle of the PROPSHEETPAGE that represents the wizard page that is before the wizard extension page.
old-location: shell\IWizardSite_GetPreviousPage.htm
old-project: shell
ms.assetid: 998eabc5-a0d4-450f-92bf-cf81f74c48d2
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetPreviousPage, GetPreviousPage method [Windows Shell], GetPreviousPage method [Windows Shell],IWizardSite interface, IWizardSite interface [Windows Shell],GetPreviousPage method, IWizardSite.GetPreviousPage, IWizardSite::GetPreviousPage, _shell_IWizardSite_GetPreviousPage, shell.IWizardSite_GetPreviousPage, shobjidl/IWizardSite::GetPreviousPage
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IWizardSite.GetPreviousPage
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IWizardSite::GetPreviousPage


## -description


Called when the user navigates backward out of the wizard extension. Gets the handle of the <a href="https://msdn.microsoft.com/69ceb9f4-f68c-4c60-9610-4c1977aae4b8">PROPSHEETPAGE</a> that represents the wizard page that is before the wizard extension page.


## -parameters




### -param phpage






#### - phPage [out]

Type: <b>HPROPSHEETPAGE*</b>

A pointer to a variable handle of type <a href="https://msdn.microsoft.com/69ceb9f4-f68c-4c60-9610-4c1977aae4b8">PROPSHEETPAGE</a> that represents the wizard page that comes immediately before the wizard extension page.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




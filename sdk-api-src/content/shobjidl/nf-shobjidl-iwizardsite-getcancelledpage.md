---
UID: NF:shobjidl.IWizardSite.GetCancelledPage
title: IWizardSite::GetCancelledPage
author: windows-sdk-content
description: Called when the user cancels navigation through the wizard extension. Gets the handle of the PROPSHEETPAGE that represents the wizard page to display when the user cancels navigation while in the wizard extension.
old-location: shell\IWizardSite_GetCancelledPage.htm
old-project: shell
ms.assetid: 682f5624-5fec-4bc9-9455-150e8e951538
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetCancelledPage, GetCancelledPage method [Windows Shell], GetCancelledPage method [Windows Shell],IWizardSite interface, IWizardSite interface [Windows Shell],GetCancelledPage method, IWizardSite.GetCancelledPage, IWizardSite::GetCancelledPage, _shell_IWizardSite_GetCancelledPage, shell.IWizardSite_GetCancelledPage, shobjidl/IWizardSite::GetCancelledPage
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IWizardSite.GetCancelledPage
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IWizardSite::GetCancelledPage


## -description


Called when the user cancels navigation through the wizard extension. Gets the handle of the <a href="https://msdn.microsoft.com/en-us/library/Bb774548(v=VS.85).aspx">PROPSHEETPAGE</a> that represents the wizard page to display when the user cancels navigation while in the wizard extension.


## -parameters




### -param phpage






#### - phPage [out]

Type: <b>HPROPSHEETPAGE*</b>

A pointer to a handle variable of type <a href="https://msdn.microsoft.com/en-us/library/Bb774548(v=VS.85).aspx">PROPSHEETPAGE</a> that receives the wizard page to display when the user cancels navigation while in the wizard extension.



## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




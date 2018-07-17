---
UID: NF:shobjidl.IWebWizardExtension.SetInitialURL
title: IWebWizardExtension::SetInitialURL
author: windows-sdk-content
description: Sets the URL of the initial server-provided HTML page in a hosted wizard.
old-location: shell\IWebWizardExtension_SetInitialURL.htm
old-project: shell
ms.assetid: 3fd0979f-2f45-4281-80df-72a4322ee219
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IWebWizardExtension interface [Windows Shell],SetInitialURL method, IWebWizardExtension.SetInitialURL, IWebWizardExtension::SetInitialURL, SetInitialURL, SetInitialURL method [Windows Shell], SetInitialURL method [Windows Shell],IWebWizardExtension interface, _shell_IWebWizardExtension_SetInitialURL, shell.IWebWizardExtension_SetInitialURL, shobjidl/IWebWizardExtension::SetInitialURL
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
 - IWebWizardExtension.SetInitialURL
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IWebWizardExtension::SetInitialURL


## -description


Sets the URL of the initial server-provided HTML page in a hosted wizard.


## -parameters




### -param pszURL [in]

Type: <b>LPCWSTR</b>

The URL of the initial server-provided HTML page.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




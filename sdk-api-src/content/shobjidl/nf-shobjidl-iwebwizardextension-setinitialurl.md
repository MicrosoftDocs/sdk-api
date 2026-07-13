---
UID: NF:shobjidl.IWebWizardExtension.SetInitialURL
title: IWebWizardExtension::SetInitialURL (shobjidl.h)
description: Sets the URL of the initial server-provided HTML page in a hosted wizard.
helpviewer_keywords: ["IWebWizardExtension interface [Windows Shell]","SetInitialURL method","IWebWizardExtension.SetInitialURL","IWebWizardExtension::SetInitialURL","SetInitialURL","SetInitialURL method [Windows Shell]","SetInitialURL method [Windows Shell]","IWebWizardExtension interface","_shell_IWebWizardExtension_SetInitialURL","shell.IWebWizardExtension_SetInitialURL","shobjidl/IWebWizardExtension::SetInitialURL"]
old-location: shell\IWebWizardExtension_SetInitialURL.htm
tech.root: shell
ms.assetid: 3fd0979f-2f45-4281-80df-72a4322ee219
ms.date: 12/05/2018
ms.keywords: IWebWizardExtension interface [Windows Shell],SetInitialURL method, IWebWizardExtension.SetInitialURL, IWebWizardExtension::SetInitialURL, SetInitialURL, SetInitialURL method [Windows Shell], SetInitialURL method [Windows Shell],IWebWizardExtension interface, _shell_IWebWizardExtension_SetInitialURL, shell.IWebWizardExtension_SetInitialURL, shobjidl/IWebWizardExtension::SetInitialURL
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
 - IWebWizardExtension::SetInitialURL
 - shobjidl/IWebWizardExtension::SetInitialURL
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
 - IWebWizardExtension.SetInitialURL
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.


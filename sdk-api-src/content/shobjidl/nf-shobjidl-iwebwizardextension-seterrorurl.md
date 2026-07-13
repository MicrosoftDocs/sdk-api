---
UID: NF:shobjidl.IWebWizardExtension.SetErrorURL
title: IWebWizardExtension::SetErrorURL (shobjidl.h)
description: Specifies the URL of a page that displays when a user experiences an error while navigating through the wizard extension pages.
helpviewer_keywords: ["IWebWizardExtension interface [Windows Shell]","SetErrorURL method","IWebWizardExtension.SetErrorURL","IWebWizardExtension::SetErrorURL","SetErrorURL","SetErrorURL method [Windows Shell]","SetErrorURL method [Windows Shell]","IWebWizardExtension interface","_shell_IWebWizardExtension_SetErrorURL","shell.IWebWizardExtension_SetErrorURL","shobjidl/IWebWizardExtension::SetErrorURL"]
old-location: shell\IWebWizardExtension_SetErrorURL.htm
tech.root: shell
ms.assetid: 4b7ba688-dfa0-45ee-a32f-08f24a7626d8
ms.date: 12/05/2018
ms.keywords: IWebWizardExtension interface [Windows Shell],SetErrorURL method, IWebWizardExtension.SetErrorURL, IWebWizardExtension::SetErrorURL, SetErrorURL, SetErrorURL method [Windows Shell], SetErrorURL method [Windows Shell],IWebWizardExtension interface, _shell_IWebWizardExtension_SetErrorURL, shell.IWebWizardExtension_SetErrorURL, shobjidl/IWebWizardExtension::SetErrorURL
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
 - IWebWizardExtension::SetErrorURL
 - shobjidl/IWebWizardExtension::SetErrorURL
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
 - IWebWizardExtension.SetErrorURL
---

# IWebWizardExtension::SetErrorURL


## -description

Specifies the URL of a page that displays when a user experiences an error while navigating through the wizard extension pages.

## -parameters

### -param pszErrorURL [in]

Type: <b>LPCWSTR</b>

The URL of the page to display.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.


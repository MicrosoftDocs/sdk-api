---
UID: NN:shobjidl.IWizardSite
title: IWizardSite (shobjidl.h)
description: Exposes methods used by a wizard extension to navigate the borders between itself and the rest of the wizard.
helpviewer_keywords: ["IWizardSite","IWizardSite interface [Windows Shell]","IWizardSite interface [Windows Shell]","described","_shell_IWizardSite","shell.IWizardSite","shobjidl/IWizardSite"]
old-location: shell\IWizardSite.htm
tech.root: shell
ms.assetid: 4c366f9c-d774-4390-8f43-8c25f86e3c35
ms.date: 12/05/2018
ms.keywords: IWizardSite, IWizardSite interface [Windows Shell], IWizardSite interface [Windows Shell],described, _shell_IWizardSite, shell.IWizardSite, shobjidl/IWizardSite
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
 - IWizardSite
 - shobjidl/IWizardSite
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
 - IWizardSite
---

# IWizardSite interface


## -description

Exposes methods used by a wizard extension to navigate the borders between itself and the rest of the wizard.

## -inheritance

The <b>IWizardSite</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWizardSite</b> also has these types of members:

## -remarks

When the user backs out or cancels the extension, or when the extension finishes displaying its pages, the extension then communicates to the wizard that it must navigate in and out of the stack of pages.

---
UID: NN:shobjidl.IWizardExtension
title: IWizardExtension (shobjidl.h)
description: Used by wizards such as the Web Publishing Wizard and Online Print Ordering Wizard which host server-side content pages. This interface exposes methods to specify supported extension pages and to navigate into and out of those pages.helpviewer_keywords: ["IWizardExtension","IWizardExtension interface [Windows Shell]","IWizardExtension interface [Windows Shell]","described","_shell_IWizardExtension","shell.IWizardExtension","shobjidl/IWizardExtension"]
old-location: shell\IWizardExtension.htm
tech.root: shell
ms.assetid: f2d69f18-73de-44c1-9543-909e509b1c4f
ms.date: 12/05/2018
ms.keywords: IWizardExtension, IWizardExtension interface [Windows Shell], IWizardExtension interface [Windows Shell],described, _shell_IWizardExtension, shell.IWizardExtension, shobjidl/IWizardExtension
f1_keywords:
- shobjidl/IWizardExtension
dev_langs:
- c++
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
- IWizardExtension
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWizardExtension interface


## -description


Used by wizards such as the Web Publishing Wizard and Online Print Ordering Wizard which host server-side content pages. This interface exposes methods to specify supported extension pages and to navigate into and out of those pages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWizardExtension</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWizardExtension</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWizardExtension</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iwizardextension-addpages">AddPages</a>
</td>
<td align="left" width="63%">
Adds extension pages to the wizard by filling an array with handles to <a href="https://docs.microsoft.com/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> structures representing those pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iwizardextension-getfirstpage">GetFirstPage</a>
</td>
<td align="left" width="63%">
Gets a handle to the first page of the wizard extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iwizardextension-getlastpage">GetLastPage</a>
</td>
<td align="left" width="63%">
Gets a handle to the final page of the wizard extension pages.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-iwebwizardextension">IWebWizardExtension</a>
 

 


---
UID: NN:shobjidl.IWizardSite
title: IWizardSite (shobjidl.h)
description: Exposes methods used by a wizard extension to navigate the borders between itself and the rest of the wizard.
old-location: shell\IWizardSite.htm
tech.root: shell
ms.assetid: 4c366f9c-d774-4390-8f43-8c25f86e3c35
ms.date: 12/05/2018
ms.keywords: IWizardSite, IWizardSite interface [Windows Shell], IWizardSite interface [Windows Shell],described, _shell_IWizardSite, shell.IWizardSite, shobjidl/IWizardSite
ms.topic: interface
f1_keywords:
- shobjidl/IWizardSite
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
- IWizardSite
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWizardSite interface


## -description


Exposes methods used by a wizard extension to navigate the borders between itself and the rest of the wizard.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWizardSite</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWizardSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWizardSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iwizardsite-getcancelledpage">GetCancelledPage</a>
</td>
<td align="left" width="63%">
Called when the user cancels navigation through the wizard extension. Gets the handle of the <a href="https://docs.microsoft.com/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> that represents the wizard page to display when the user cancels navigation while in the wizard extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iwizardsite-getnextpage">GetNextPage</a>
</td>
<td align="left" width="63%">
Called when the user navigates forward past the wizard extension pages. Gets the handle of the <a href="https://docs.microsoft.com/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> that represents the wizard page immediately following the wizard extension page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iwizardsite-getpreviouspage">GetPreviousPage</a>
</td>
<td align="left" width="63%">
Called when the user navigates backward out of the wizard extension. Gets the handle of the <a href="https://docs.microsoft.com/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> that represents the wizard page that is before the wizard extension page.

</td>
</tr>
</table> 


## -remarks



When the user backs out or cancels the extension, or when the extension finishes displaying its pages, the extension then communicates to the wizard that it must navigate in and out of the stack of pages.




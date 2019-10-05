---
UID: NN:shobjidl.IWebWizardExtension
title: IWebWizardExtension (shobjidl.h)
author: windows-sdk-content
description: Extends the IWizardExtension interface by exposing methods to set the wizard extension's initial URL, and a specific URL in case of an error.
old-location: shell\IWebWizardExtension.htm
tech.root: shell
ms.assetid: f1b5f53a-3163-486f-bbe9-a8fc6b244591
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWebWizardExtension, IWebWizardExtension interface [Windows Shell], IWebWizardExtension interface [Windows Shell],described, _shell_IWebWizardExtension, shell.IWebWizardExtension, shobjidl/IWebWizardExtension
ms.topic: interface
f1_keywords: 
 - "shobjidl/IWebWizardExtension"
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
 - IWebWizardExtension
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWebWizardExtension interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-iwizardextension">IWizardExtension</a> interface by exposing methods to set the wizard extension's initial URL, and a specific URL in case of an error.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWebWizardExtension</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-iwizardextension">IWizardExtension</a>. <b>IWebWizardExtension</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWebWizardExtension</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iwebwizardextension-seterrorurl">SetErrorURL</a>
</td>
<td align="left" width="63%">
Specifies the URL of a page that displays when a user experiences an error while navigating through the wizard extension pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iwebwizardextension-setinitialurl">SetInitialURL</a>
</td>
<td align="left" width="63%">
Sets the URL of the initial server-provided HTML page in a hosted wizard.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-iwizardextension">IWizardExtension</a>
 

 


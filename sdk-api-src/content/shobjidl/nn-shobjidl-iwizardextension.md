---
UID: NN:shobjidl.IWizardExtension
title: IWizardExtension
author: windows-sdk-content
description: Used by wizards such as the Web Publishing Wizard and Online Print Ordering Wizard which host server-side content pages. This interface exposes methods to specify supported extension pages and to navigate into and out of those pages.
old-location: shell\IWizardExtension.htm
tech.root: shell
ms.assetid: f2d69f18-73de-44c1-9543-909e509b1c4f
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IWizardExtension, IWizardExtension interface [Windows Shell], IWizardExtension interface [Windows Shell],described, _shell_IWizardExtension, shell.IWizardExtension, shobjidl/IWizardExtension
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWizardExtension interface


## -description


Used by wizards such as the Web Publishing Wizard and Online Print Ordering Wizard which host server-side content pages. This interface exposes methods to specify supported extension pages and to navigate into and out of those pages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWizardExtension</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWizardExtension</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2d9a5012-3b5e-4e55-984b-70a932bab569">AddPages</a>
</td>
<td align="left" width="63%">
Adds extension pages to the wizard by filling an array with handles to <a href="https://msdn.microsoft.com/en-us/library/Bb774548(v=VS.85).aspx">PROPSHEETPAGE</a> structures representing those pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1276b63d-6d5e-4e60-b936-b307cd922b4b">GetFirstPage</a>
</td>
<td align="left" width="63%">
Gets a handle to the first page of the wizard extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4fc1089-d0fb-406d-bf05-b43b3f2cc87e">GetLastPage</a>
</td>
<td align="left" width="63%">
Gets a handle to the final page of the wizard extension pages.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f1b5f53a-3163-486f-bbe9-a8fc6b244591">IWebWizardExtension</a>
 

 


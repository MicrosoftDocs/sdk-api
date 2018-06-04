---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWebWizardExtension interface


## -description


Extends the <a href="https://msdn.microsoft.com/f2d69f18-73de-44c1-9543-909e509b1c4f">IWizardExtension</a> interface by exposing methods to set the wizard extension's initial URL, and a specific URL in case of an error.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWebWizardExtension</b> interface inherits from <a href="https://msdn.microsoft.com/f2d69f18-73de-44c1-9543-909e509b1c4f">IWizardExtension</a>. <b>IWebWizardExtension</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4b7ba688-dfa0-45ee-a32f-08f24a7626d8">SetErrorURL</a>
</td>
<td align="left" width="63%">
Specifies the URL of a page that displays when a user experiences an error while navigating through the wizard extension pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3fd0979f-2f45-4281-80df-72a4322ee219">SetInitialURL</a>
</td>
<td align="left" width="63%">
Sets the URL of the initial server-provided HTML page in a hosted wizard.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f2d69f18-73de-44c1-9543-909e509b1c4f">IWizardExtension</a>
 

 


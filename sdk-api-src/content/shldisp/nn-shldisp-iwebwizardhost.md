---
UID: NN:shldisp.IWebWizardHost
title: IWebWizardHost
author: windows-sdk-content
description: Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.
old-location: shell\WebWizardHost.htm
old-project: shell
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IWebWizardHost, WebWizardHost, WebWizardHost object [Windows Shell], WebWizardHost object [Windows Shell],described, _shell_WebWizardHost, shell.WebWizardHost, shldisp/WebWizardHost
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shldisp.h
api_name:
 - WebWizardHost
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IWebWizardHost interface


## -description


Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">WebWizardHost</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>WebWizardHost</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a>
</td>
<td align="left" width="63%">
Simulates a <b>Cancel</b> button click.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0616388-cf94-4433-ae52-24f02f1d15ac">FinalBack</a>
</td>
<td align="left" width="63%">
Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0699eb16-d6ef-46e3-bd02-d35512536275">FinalNext</a>
</td>
<td align="left" width="63%">
Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e627de44-9929-4e08-9fd9-ca22743f434a">SetHeaderText</a>
</td>
<td align="left" width="63%">
Sets the title and subtitle that appear in the wizard header. In general, the client will display the header above the HTML and below the title bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/863aa667-454c-40cd-8091-9bb456047b6c">SetWizardButtons</a>
</td>
<td align="left" width="63%">
Updates the <b>Back</b>, <b>Next</b>, and <b>Finish</b> buttons in the client's wizard frame.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">WebWizardHost</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/85b9d374-536a-4647-ba64-a0864ce25eb6">Caption</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bb0b3296-a07b-458f-bea3-e1c9ada3246b">Property</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a property's current value.

</td>
</tr>
</table> 


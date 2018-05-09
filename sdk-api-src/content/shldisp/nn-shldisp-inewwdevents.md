---
UID: NN:shldisp.INewWDEvents
title: INewWDEvents
author: windows-driver-content
description: Extends the WebWizardHost object by enabling server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.
old-location: shell\NewWDEvents.htm
old-project: shell
ms.assetid: 44f2431c-82a2-4142-bf20-55fdd0c88008
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: INewWDEvents, NewWDEvents, NewWDEvents object [Windows Shell], NewWDEvents object [Windows Shell],described, _shell_NewWDEvents, shell.NewWDEvents, shldisp/NewWDEvents
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	NewWDEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# INewWDEvents interface


## -description


Extends the <a href="https://msdn.microsoft.com/7b3690dc-2007-43a0-80a3-4a68e3c8464d">WebWizardHost</a> object by enabling server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">NewWDEvents</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>NewWDEvents</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b99eb84-c434-489a-b177-1e00f18d2dcc">PassportAuthenticate</a>
</td>
<td align="left" width="63%">
Enables server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.

</td>
</tr>
</table> 


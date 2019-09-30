---
UID: NN:shlobj.IADesktopP2
title: IADesktopP2 (shlobj.h)
author: windows-sdk-content
description: Provides methods to manage the Windows Desktop.
old-location: lwef\iadesktopp2.htm
tech.root: lwef
ms.assetid: f67cc6c0-183c-4da2-9648-68a86dccfd78
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IADesktopP2, IADesktopP2 interface [Legacy Windows Environment Features], IADesktopP2 interface [Legacy Windows Environment Features],described, _win32_IADesktopP2, lwef.iadesktopp2, shell.iadesktopp2, shlobj/IADesktopP2
ms.topic: interface
f1_keywords: 
 - "shlobj/IADesktopP2"
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IADesktopP2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADesktopP2 interface


## -description


Provides methods to manage the Windows Desktop.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADesktopP2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IADesktopP2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IADesktopP2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-iadesktopp2-updatealldesktopsubscriptions">UpdateAllDesktopSubscriptions</a>
</td>
<td align="left" width="63%">
Calls the <a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-updatealldesktopsubscriptions">UpdateAllDesktopSubscriptions</a> function to update desktop subscriptions.

</td>
</tr>
</table> 


## -remarks



Despite its name, this interface does not inherit from <a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nn-shlobj-iactivedesktopp">IActiveDesktopP</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/lwef/active-desktop-interface">Using the Active Desktop Object</a>
 

 


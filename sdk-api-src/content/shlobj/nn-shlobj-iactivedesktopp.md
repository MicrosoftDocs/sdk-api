---
UID: NN:shlobj.IActiveDesktopP
title: IActiveDesktopP (shlobj.h)
description: Exposes methods that manage the Windows Desktop.
helpviewer_keywords: ["IActiveDesktopP","IActiveDesktopP interface [Legacy Windows Environment Features]","IActiveDesktopP interface [Legacy Windows Environment Features]","described","_win32_IActiveDesktopP","lwef.iactivedesktopp","shell.iactivedesktopp","shlobj/IActiveDesktopP"]
old-location: lwef\iactivedesktopp.htm
tech.root: lwef
ms.assetid: 04d2e14a-374b-405d-803b-0bd6f57c077a
ms.date: 12/05/2018
ms.keywords: IActiveDesktopP, IActiveDesktopP interface [Legacy Windows Environment Features], IActiveDesktopP interface [Legacy Windows Environment Features],described, _win32_IActiveDesktopP, lwef.iactivedesktopp, shell.iactivedesktopp, shlobj/IActiveDesktopP
f1_keywords:
- shlobj/IActiveDesktopP
dev_langs:
- c++
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
- IActiveDesktopP
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IActiveDesktopP interface


## -description


<p class="CCE_Message">[<b>IActiveDesktopP</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Exposes methods that manage the Windows Desktop.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActiveDesktopP</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IActiveDesktopP</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IActiveDesktopP</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-iactivedesktopp-setsafemode">SetSafeMode</a>
</td>
<td align="left" width="63%">
Sets or updates the Active Desktop to safe mode.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/lwef/active-desktop-interface">Using the Active Desktop Object</a>
 

 


---
UID: NN:shlobj.IDocViewSite
title: IDocViewSite (shlobj.h)
description: Used as a site object by the IShellView interface.
old-location: shell\IDocViewSite.htm
tech.root: shell
ms.assetid: 031e0079-842e-4357-acb2-5d1160094e18
ms.date: 12/05/2018
ms.keywords: IDocViewSite, IDocViewSite interface [Windows Shell], IDocViewSite interface [Windows Shell],described, _win32_IDocViewSite, shell.IDocViewSite, shlobj/IDocViewSite
ms.topic: interface
f1_keywords:
- shlobj/IDocViewSite
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
- IDocViewSite
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDocViewSite interface


## -description


<p class="CCE_Message">[This interface is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be unsupported in subsequent versions of Windows.]

Used as a site object by the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDocViewSite</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDocViewSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDocViewSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-idocviewsite-onsettitle">OnSetTitle</a>
</td>
<td align="left" width="63%">
Sets or retrieves the title of the site object.

</td>
</tr>
</table> 


## -remarks



You can call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method on <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> to get a pointer to the <b>IDocViewSite</b> interface.




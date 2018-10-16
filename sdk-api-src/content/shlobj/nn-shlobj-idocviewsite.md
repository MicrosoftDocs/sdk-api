---
UID: NN:shlobj.IDocViewSite
title: IDocViewSite
author: windows-sdk-content
description: Used as a site object by the IShellView interface.
old-location: shell\IDocViewSite.htm
tech.root: shell
ms.assetid: 031e0079-842e-4357-acb2-5d1160094e18
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IDocViewSite, IDocViewSite interface [Windows Shell], IDocViewSite interface [Windows Shell],described, _win32_IDocViewSite, shell.IDocViewSite, shlobj/IDocViewSite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDocViewSite interface


## -description


<p class="CCE_Message">[This interface is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be unsupported in subsequent versions of Windows.]

Used as a site object by the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDocViewSite</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDocViewSite</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/941a8fe0-27db-4646-97d0-287fc94e7721">OnSetTitle</a>
</td>
<td align="left" width="63%">
Sets or retrieves the title of the site object.

</td>
</tr>
</table> 


## -remarks



You can call the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method on <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> to get a pointer to the <b>IDocViewSite</b> interface.




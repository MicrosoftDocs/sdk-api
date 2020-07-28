---
UID: NN:shlobj.IFileViewerSite
title: IFileViewerSite (shlobj.h)
description: Exposes methods that designate an interface that allows a file viewer to retrieve the handle to the current pinned window, or to set a new pinned window.
helpviewer_keywords: ["IFileViewerSite","IFileViewerSite interface [Windows Shell]","IFileViewerSite interface [Windows Shell]","described","_win32_IFileViewerSite","shell.IFileViewerSite","shlobj/IFileViewerSite"]
old-location: shell\IFileViewerSite.htm
tech.root: shell
ms.assetid: 500fa3e4-1865-4543-ae34-8bd7ce9d94cb
ms.date: 12/05/2018
ms.keywords: IFileViewerSite, IFileViewerSite interface [Windows Shell], IFileViewerSite interface [Windows Shell],described, _win32_IFileViewerSite, shell.IFileViewerSite, shlobj/IFileViewerSite
f1_keywords:
- shlobj/IFileViewerSite
dev_langs:
- c++
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IFileViewerSite
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileViewerSite interface


## -description


Exposes methods that designate an interface that allows a file viewer to retrieve the handle to the current pinned window, or to set a new pinned window. The pinned window is the window in which the current file viewer displays a file. When the user selects a new file to view, the Shell directs the file viewer to display the new file in the pinned window rather than create a new window.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileViewerSite</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileViewerSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileViewerSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-ifileviewersite-getpinnedwindow">GetPinnedWindow</a>
</td>
<td align="left" width="63%">
Gets the handle to the current pinned window, if one exists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-ifileviewersite-setpinnedwindow">SetPinnedWindow</a>
</td>
<td align="left" width="63%">
Sets the pinned window. When the user selects a new file to view, the Shell directs the file viewer to display the new file in the pinned window instead of creating a new window.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  File viewers are not supported by Windows 2000 and later systems.</div>
<div> </div>
You do not typically implement this interface. The Shell implements this interface to provide a pinned window for the file viewer.

You use this interface to obtain or set the window for a file viewer.




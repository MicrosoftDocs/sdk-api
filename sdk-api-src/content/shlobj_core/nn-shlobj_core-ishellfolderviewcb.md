---
UID: NN:shlobj_core.IShellFolderViewCB
title: IShellFolderViewCB
author: windows-sdk-content
description: Exposes a method that allows communication between Windows Explorer and a folder view implemented using the system folder view object (the IShellView object returned through SHCreateShellFolderView) so that the folder view can be notified of events and modify its view accordingly.
old-location: shell\IShellFolderViewCB.htm
tech.root: shell
ms.assetid: 0cd2bce8-d77a-4140-869b-707aaa279796
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IShellFolderViewCB, IShellFolderViewCB interface [Windows Shell], IShellFolderViewCB interface [Windows Shell],described, _win32_IShellFolderViewCB, shell.IShellFolderViewCB, shlobj_core/IShellFolderViewCB
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shlobj_core.h
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
req.lib: Shell32.lib
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
 - IShellFolderViewCB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderViewCB interface


## -description


Exposes a method that allows communication between Windows Explorer and a folder view implemented using the system folder view object (the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> object returned through <a href="https://msdn.microsoft.com/f2948a6d-84a5-456b-b328-ba76dba46e9d">SHCreateShellFolderView</a>) so that the folder view can be notified of events and modify its view accordingly.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellFolderViewCB</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellFolderViewCB</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellFolderViewCB</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1678dd76-6ed4-4625-9170-22dcd3d7e8d2">MessageSFVCB</a>
</td>
<td align="left" width="63%">
Allows communication between the system folder view object and a system folder view callback object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/744c2b49-017e-4284-a39b-3d317e483316">LPFNVIEWCALLBACK</a>
 

 


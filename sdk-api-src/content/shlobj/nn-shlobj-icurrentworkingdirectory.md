---
UID: NN:shlobj.ICurrentWorkingDirectory
title: ICurrentWorkingDirectory (shlobj.h)
author: windows-sdk-content
description: Exposes methods that enable a client to retrieve or set an object's current working directory.
old-location: shell\ICurrentWorkingDirectory.htm
tech.root: shell
ms.assetid: 1fdbe616-3ca3-4f07-b89c-4c76561ba169
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICurrentWorkingDirectory, ICurrentWorkingDirectory interface [Windows Shell], ICurrentWorkingDirectory interface [Windows Shell],described, _win32_ICurrentWorkingDirectory, shell.ICurrentWorkingDirectory, shlobj/ICurrentWorkingDirectory
ms.topic: interface
f1_keywords: ["shlobj/ICurrentWorkingDirectory"]
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ICurrentWorkingDirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICurrentWorkingDirectory interface


## -description


Exposes methods that enable a client to retrieve or set an object's current working directory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICurrentWorkingDirectory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICurrentWorkingDirectory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICurrentWorkingDirectory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-icurrentworkingdirectory-getdirectory">GetDirectory</a>
</td>
<td align="left" width="63%">
Gets the current working directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-icurrentworkingdirectory-setdirectory">SetDirectory</a>
</td>
<td align="left" width="63%">
Sets the current working directory.

</td>
</tr>
</table> 


## -remarks



Implement this interface if your object allows clients to retrieve or set the current working directory.

Use this interface to retrieve or set the working directory of the object that exports it.




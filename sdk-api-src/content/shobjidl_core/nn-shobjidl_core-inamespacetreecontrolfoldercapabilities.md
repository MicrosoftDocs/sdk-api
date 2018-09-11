---
UID: NN:shobjidl_core.INameSpaceTreeControlFolderCapabilities
title: INameSpaceTreeControlFolderCapabilities
author: windows-sdk-content
description: Exposes a single method that retrieves the status of a folder's System.IsPinnedToNameSpaceTree filtering support.
old-location: shell\INameSpaceTreeControlFolderCapabilities.htm
tech.root: shell
ms.assetid: 2a5580f6-42cb-46c7-9507-a59d36b2cd91
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: INameSpaceTreeControlFolderCapabilities, INameSpaceTreeControlFolderCapabilities interface [Windows Shell], INameSpaceTreeControlFolderCapabilities interface [Windows Shell],described, _shell_INameSpaceTreeControlFolderCapabilities, shell.INameSpaceTreeControlFolderCapabilities, shobjidl_core/INameSpaceTreeControlFolderCapabilities
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - INameSpaceTreeControlFolderCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeControlFolderCapabilities interface


## -description


Exposes a single method that retrieves the status of a folder's <a href="https://msdn.microsoft.com/00937acb-1ce2-44f6-96a1-69e5dbb665f6">System.IsPinnedToNameSpaceTree</a> filtering support.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INameSpaceTreeControlFolderCapabilities</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INameSpaceTreeControlFolderCapabilities</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INameSpaceTreeControlFolderCapabilities</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1534431c-21fc-4eb9-8f17-ddd7414bef94">GetFolderCapabilities</a>
</td>
<td align="left" width="63%">
Gets a folder's capability to be filtered through the <a href="https://msdn.microsoft.com/00937acb-1ce2-44f6-96a1-69e5dbb665f6">System.IsPinnedToNameSpaceTree</a> property key value and change notification registration status.

</td>
</tr>
</table> 


## -remarks



The namespace tree control checks all the nodes it enumerates to see if they support filtering. This is done by retrieving the <a href="https://msdn.microsoft.com/00937acb-1ce2-44f6-96a1-69e5dbb665f6">System.IsPinnedToNameSpaceTree</a> property for the shell folders that support this interface. Nodes that do not support this interface do not have filtering support and are shown by default.

Use this interface to retrieve the filtering support status of a shell folder.




---
UID: NN:shobjidl_core.IDataTransferManagerInterop
title: IDataTransferManagerInterop
author: windows-sdk-content
description: Enables access to DataTransferManager methods in a Windows Store app that manages multiple windows.
old-location: shell\idatatransfermanagerinterop.htm
tech.root: shell
ms.assetid: C4F49401-C863-4D3B-80EE-D36F714E7D90
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDataTransferManagerInterop, IDataTransferManagerInterop interface [Windows Shell], IDataTransferManagerInterop interface [Windows Shell],described, shell.idatatransfermanagerinterop, shobjidl_core/IDataTransferManagerInterop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [UWP apps only]
req.target-min-winversvr: Windows Server 2012 [UWP apps only]
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
 - IDataTransferManagerInterop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataTransferManagerInterop interface


## -description


Enables access to <a href="https://msdn.microsoft.com/21a12246-a49e-4f1e-b539-c35164b488d7">DataTransferManager</a> methods in a Windows Store app that manages multiple windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataTransferManagerInterop</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDataTransferManagerInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDataTransferManagerInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/129CEEBF-0D02-4746-8F9B-4F5F5A95E6A2">GetForWindow</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/21a12246-a49e-4f1e-b539-c35164b488d7">DataTransferManager</a> instance for the specified window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/095AE176-5EA1-470E-AA4A-ACD91AF54E5D">ShowShareUIForWindow</a>
</td>
<td align="left" width="63%">
Displays the UI for sharing content for the specified window.

</td>
</tr>
</table> 


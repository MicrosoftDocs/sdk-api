---
UID: NN:shobjidl_core.IDataTransferManagerInterop
title: IDataTransferManagerInterop (shobjidl_core.h)
description: Enables access to DataTransferManager methods in a Windows Store app that manages multiple windows.helpviewer_keywords: ["IDataTransferManagerInterop","IDataTransferManagerInterop interface [Windows Shell]","IDataTransferManagerInterop interface [Windows Shell]","described","shell.idatatransfermanagerinterop","shobjidl_core/IDataTransferManagerInterop"]
old-location: shell\idatatransfermanagerinterop.htm
tech.root: shell
ms.assetid: C4F49401-C863-4D3B-80EE-D36F714E7D90
ms.date: 12/05/2018
ms.keywords: IDataTransferManagerInterop, IDataTransferManagerInterop interface [Windows Shell], IDataTransferManagerInterop interface [Windows Shell],described, shell.idatatransfermanagerinterop, shobjidl_core/IDataTransferManagerInterop
f1_keywords:
- shobjidl_core/IDataTransferManagerInterop
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataTransferManagerInterop interface


## -description


Enables access to <a href="https://docs.microsoft.com/uwp/api/windows.applicationmodel.datatransfer.datatransfermanager">DataTransferManager</a> methods in a Windows Store app that manages multiple windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataTransferManagerInterop</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDataTransferManagerInterop</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idatatransfermanagerinterop-getforwindow">GetForWindow</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/uwp/api/windows.applicationmodel.datatransfer.datatransfermanager">DataTransferManager</a> instance for the specified window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idatatransfermanagerinterop-showshareuiforwindow">ShowShareUIForWindow</a>
</td>
<td align="left" width="63%">
Displays the UI for sharing content for the specified window.

</td>
</tr>
</table> 


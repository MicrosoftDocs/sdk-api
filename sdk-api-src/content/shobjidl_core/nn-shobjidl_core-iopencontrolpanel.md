---
UID: NN:shobjidl_core.IOpenControlPanel
title: IOpenControlPanel (shobjidl_core.h)
description: Exposes methods that retrieve the view state of the Control Panel, the path of individual Control Panel items, and that open either the Control Panel itself or an individual Control Panel item.
helpviewer_keywords: ["IOpenControlPanel","IOpenControlPanel interface [Windows Shell]","IOpenControlPanel interface [Windows Shell]","described","_shell_IOpenControlPanel","shell.IOpenControlPanel","shobjidl_core/IOpenControlPanel"]
old-location: shell\IOpenControlPanel.htm
tech.root: shell
ms.assetid: fbf86553-7aa1-4a0f-9775-5f71f41b1705
ms.date: 12/05/2018
ms.keywords: IOpenControlPanel, IOpenControlPanel interface [Windows Shell], IOpenControlPanel interface [Windows Shell],described, _shell_IOpenControlPanel, shell.IOpenControlPanel, shobjidl_core/IOpenControlPanel
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOpenControlPanel
 - shobjidl_core/IOpenControlPanel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IOpenControlPanel
---

# IOpenControlPanel interface


## -description

Exposes methods that retrieve the view state of the Control Panel, the path of individual Control Panel items, and that open either the Control Panel itself or an individual Control Panel item.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpenControlPanel</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpenControlPanel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpenControlPanel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-getcurrentview">GetCurrentView</a>
</td>
<td align="left" width="63%">
Gets the most recent Control Panel view: Classic view or Category view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-getpath">GetPath</a>
</td>
<td align="left" width="63%">
Gets the path of a specified Control Panel item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open">Open</a>
</td>
<td align="left" width="63%">
Opens the specified Control Panel item, optionally to a specific page.

</td>
</tr>
</table>


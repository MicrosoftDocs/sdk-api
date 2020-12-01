---
UID: NN:shobjidl.IFileDialogControlEvents
title: IFileDialogControlEvents (shobjidl.h)
description: Exposes methods that allow an application to be notified of events that are related to controls that the application has added to a common file dialog.
helpviewer_keywords: ["IFileDialogControlEvents","IFileDialogControlEvents interface [Windows Shell]","IFileDialogControlEvents interface [Windows Shell]","described","shell.IFileDialogControlEvents","shell_IFileDialogControlEvents","shobjidl/IFileDialogControlEvents"]
old-location: shell\IFileDialogControlEvents.htm
tech.root: shell
ms.assetid: 745ee176-53bc-4388-beaa-a0856a438ee6
ms.date: 12/05/2018
ms.keywords: IFileDialogControlEvents, IFileDialogControlEvents interface [Windows Shell], IFileDialogControlEvents interface [Windows Shell],described, shell.IFileDialogControlEvents, shell_IFileDialogControlEvents, shobjidl/IFileDialogControlEvents
req.header: shobjidl.h
req.include-header: 
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
 - IFileDialogControlEvents
 - shobjidl/IFileDialogControlEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IFileDialogControlEvents
---

# IFileDialogControlEvents interface


## -description

Exposes methods that allow an application to be notified of events that are related to controls that the application has added to a common file dialog.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileDialogControlEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileDialogControlEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileDialogControlEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl/nf-shobjidl-ifiledialogcontrolevents-onbuttonclicked">OnButtonClicked</a>
</td>
<td align="left" width="63%">
Called when the user clicks a command button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl/nf-shobjidl-ifiledialogcontrolevents-oncheckbuttontoggled">OnCheckButtonToggled</a>
</td>
<td align="left" width="63%">
Called when the user changes the state of a check button (check box).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl/nf-shobjidl-ifiledialogcontrolevents-oncontrolactivating">OnControlActivating</a>
</td>
<td align="left" width="63%">
Called when an <b>Open</b> button drop-down list customized through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-enableopendropdown">IFileDialogCustomize::EnableOpenDropDown</a> or a <b>Tools</b> menu is about to display its contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl/nf-shobjidl-ifiledialogcontrolevents-onitemselected">OnItemSelected</a>
</td>
<td align="left" width="63%">
Called when an item is selected in a combo box, when a user clicks an option button (also known as a radio button), or an item is chosen from the <b>Tools</b> menu.

</td>
</tr>
</table>

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
<b>IFileDialogControlEvents</b> is implemented by an application on the same object that it implements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents">IFileDialogEvents</a> in.

The dialog does not check the return values of this interface's methods.
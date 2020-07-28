---
UID: NN:shobjidl_core.IFileDialogCustomize
title: IFileDialogCustomize (shobjidl_core.h)
description: Exposes methods that allow an application to add controls to a common file dialog.
helpviewer_keywords: ["IFileDialogCustomize","IFileDialogCustomize interface [Windows Shell]","IFileDialogCustomize interface [Windows Shell]","described","shell.IFileDialogCustomize","shell_IFileDialogCustomize","shobjidl_core/IFileDialogCustomize"]
old-location: shell\IFileDialogCustomize.htm
tech.root: shell
ms.assetid: f1c29688-3538-40ff-a1da-6211cc5dded7
ms.date: 12/05/2018
ms.keywords: IFileDialogCustomize, IFileDialogCustomize interface [Windows Shell], IFileDialogCustomize interface [Windows Shell],described, shell.IFileDialogCustomize, shell_IFileDialogCustomize, shobjidl_core/IFileDialogCustomize
f1_keywords:
- shobjidl_core/IFileDialogCustomize
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IFileDialogCustomize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileDialogCustomize interface


## -description


Exposes methods that allow an application to add controls to a common file dialog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileDialogCustomize</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileDialogCustomize</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileDialogCustomize</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-addcheckbutton">AddCheckButton</a>
</td>
<td align="left" width="63%">
Adds a check button (check box) to the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-addcombobox">AddComboBox</a>
</td>
<td align="left" width="63%">
Adds a combo box to the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-addcontrolitem">AddControlItem</a>
</td>
<td align="left" width="63%">
Adds an item to a container control in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-addeditbox">AddEditBox</a>
</td>
<td align="left" width="63%">
Adds an edit box control to the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-addmenu">AddMenu</a>
</td>
<td align="left" width="63%">
Adds a menu to the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-addpushbutton">AddPushButton</a>
</td>
<td align="left" width="63%">
Adds a button to the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-addradiobuttonlist">AddRadioButtonList</a>
</td>
<td align="left" width="63%">
Adds an option button (also known as radio button) group to the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-addseparator">AddSeparator</a>
</td>
<td align="left" width="63%">
Adds a separator to the dialog, allowing a visual separation of controls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-addtext">AddText</a>
</td>
<td align="left" width="63%">
Adds text content to the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-enableopendropdown">EnableOpenDropDown</a>
</td>
<td align="left" width="63%">
Enables a drop-down list on the <b>Open</b> or <b>Save</b> button in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-endvisualgroup">EndVisualGroup</a>
</td>
<td align="left" width="63%">
Stops the addition of elements to a visual group in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-getcheckbuttonstate">GetCheckButtonState</a>
</td>
<td align="left" width="63%">
Gets the current state of a check button (check box) in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-getcontrolitemstate">GetControlItemState</a>
</td>
<td align="left" width="63%">
Gets the current state of an item in a container control found in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-getcontrolstate">GetControlState</a>
</td>
<td align="left" width="63%">
Gets the current visibility and enabled states of a given control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-geteditboxtext">GetEditBoxText</a>
</td>
<td align="left" width="63%">
Gets the current text in an edit box control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-getselectedcontrolitem">GetSelectedControlItem</a>
</td>
<td align="left" width="63%">
Gets a particular item from specified container controls in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-makeprominent">MakeProminent</a>
</td>
<td align="left" width="63%">
Places a control in the dialog so that it stands out compared to other added controls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-removeallcontrolitems">RemoveAllControlItems</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-removecontrolitem">RemoveControlItem</a>
</td>
<td align="left" width="63%">
Removes an item from a container control in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-setcheckbuttonstate">SetCheckButtonState</a>
</td>
<td align="left" width="63%">
Sets the state of a check button (check box) in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-setcontrolitemstate">SetControlItemState</a>
</td>
<td align="left" width="63%">
Sets the current state of an item in a container control found in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-setcontrolitemtext">SetControlItemText</a>
</td>
<td align="left" width="63%">
Sets the text of a control item. For example, the text that accompanies a radio button or an item in a menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-setcontrollabel">SetControlLabel</a>
</td>
<td align="left" width="63%">
Sets the text associated with a control, such as button text or an edit box label.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-setcontrolstate">SetControlState</a>
</td>
<td align="left" width="63%">
Sets the current visibility and enabled states of a given control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-seteditboxtext">SetEditBoxText</a>
</td>
<td align="left" width="63%">
Sets the text in an edit box control found in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-setselectedcontrolitem">SetSelectedControlItem</a>
</td>
<td align="left" width="63%">
Sets the selected state of a particular item in an option button group or a combo box found in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-startvisualgroup">StartVisualGroup</a>
</td>
<td align="left" width="63%">
Declares a visual group in the dialog. Subsequent calls to any "add" method add those elements to this group.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>

<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-ifiledialogcontrolevents">IFileDialogControlEvents</a> is implemented on the file dialog object.

Controls are added to the dialog before the dialog is shown. Their layout is implied by the order in which they are added. Once the dialog is shown, controls cannot be added or removed, but the existing controls can be hidden or disabled at any time. Their labels can also be changed at any time.

Container controls are controls that can have items added to them. Container controls include combo boxes, menus, the drop-down list attached to the <b>Open</b> button, and any option button groups. The order that items appear in a container is the order in which they were added. There is no facility for reordering them. IDs are scoped to the parent control. Container controls, with the exception of menus, have a selected item.

Items with a container control cannot be changed after they have been created, except for their enabled and visible states. However, they can be added and removed at any time. For example, if you needed to change the text of a menu, you would have to remove the current menu and add another with the correct text.




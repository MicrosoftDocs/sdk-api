---
UID: NN:shobjidl_core.IFileDialogCustomize
title: IFileDialogCustomize
author: windows-sdk-content
description: Exposes methods that allow an application to add controls to a common file dialog.
old-location: shell\IFileDialogCustomize.htm
tech.root: shell
ms.assetid: f1c29688-3538-40ff-a1da-6211cc5dded7
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IFileDialogCustomize, IFileDialogCustomize interface [Windows Shell], IFileDialogCustomize interface [Windows Shell],described, shell.IFileDialogCustomize, shell_IFileDialogCustomize, shobjidl_core/IFileDialogCustomize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialogCustomize interface


## -description


Exposes methods that allow an application to add controls to a common file dialog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileDialogCustomize</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFileDialogCustomize</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/273ec875-43c1-454f-a4fc-01a513554e68">AddCheckButton</a>
</td>
<td align="left" width="63%">
Adds a check button (check box) to the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fdb7d682-5182-4bc0-b256-5073bd55c96d">AddComboBox</a>
</td>
<td align="left" width="63%">
Adds a combo box to the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56d7d0df-0c3e-4bc3-b91e-3b191f5dad76">AddControlItem</a>
</td>
<td align="left" width="63%">
Adds an item to a container control in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7648eb7a-d7c4-4d4f-a347-52eb81135270">AddEditBox</a>
</td>
<td align="left" width="63%">
Adds an edit box control to the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5e29554-e095-4164-bf67-64f9d6a3e502">AddMenu</a>
</td>
<td align="left" width="63%">
Adds a menu to the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd0e4a8f-59c7-4056-8521-abb4c8c08a40">AddPushButton</a>
</td>
<td align="left" width="63%">
Adds a button to the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f60b69d-4625-48b7-b265-ab2e9d842fc2">AddRadioButtonList</a>
</td>
<td align="left" width="63%">
Adds an option button (also known as radio button) group to the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2d0f1c7-9296-4651-8910-89dcfe5a6a68">AddSeparator</a>
</td>
<td align="left" width="63%">
Adds a separator to the dialog, allowing a visual separation of controls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/efea2fdb-4006-4567-b53c-faa891d18c7e">AddText</a>
</td>
<td align="left" width="63%">
Adds text content to the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4626030-0fc7-4329-b897-01f4ce8728a0">EnableOpenDropDown</a>
</td>
<td align="left" width="63%">
Enables a drop-down list on the <b>Open</b> or <b>Save</b> button in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84aef9e1-2b70-4e8b-b261-cc49f8e65ead">EndVisualGroup</a>
</td>
<td align="left" width="63%">
Stops the addition of elements to a visual group in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c16643e5-a711-455a-8967-2c810e28ea60">GetCheckButtonState</a>
</td>
<td align="left" width="63%">
Gets the current state of a check button (check box) in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62fc28c4-3e6d-4141-b5c7-e7659a1a15c2">GetControlItemState</a>
</td>
<td align="left" width="63%">
Gets the current state of an item in a container control found in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a167050-2778-4cc2-9b05-ec81f679c6c0">GetControlState</a>
</td>
<td align="left" width="63%">
Gets the current visibility and enabled states of a given control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c3db511-d357-48b4-9ac3-07f6b3d23a5f">GetEditBoxText</a>
</td>
<td align="left" width="63%">
Gets the current text in an edit box control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1dd33779-071f-484e-9d89-1cc64ea03293">GetSelectedControlItem</a>
</td>
<td align="left" width="63%">
Gets a particular item from specified container controls in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e7b1573-cbd7-49eb-a26d-e2aba0bb4495">MakeProminent</a>
</td>
<td align="left" width="63%">
Places a control in the dialog so that it stands out compared to other added controls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b706b8a-9c67-4f76-8ebe-af412fcd14cd">RemoveAllControlItems</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/190aaeba-817d-421c-a356-157f3ae7d2e1">RemoveControlItem</a>
</td>
<td align="left" width="63%">
Removes an item from a container control in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b028a811-e559-4152-9081-abaec0cab347">SetCheckButtonState</a>
</td>
<td align="left" width="63%">
Sets the state of a check button (check box) in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2570b717-b886-4139-837b-5d71ec16c21e">SetControlItemState</a>
</td>
<td align="left" width="63%">
Sets the current state of an item in a container control found in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d89f67ee-ff56-4810-9627-e8f35e653ff4">SetControlItemText</a>
</td>
<td align="left" width="63%">
Sets the text of a control item. For example, the text that accompanies a radio button or an item in a menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/369038ad-999b-425c-bd47-b6a06e5f6939">SetControlLabel</a>
</td>
<td align="left" width="63%">
Sets the text associated with a control, such as button text or an edit box label.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53b9a65d-2219-45d0-9367-b9ea3e87cd70">SetControlState</a>
</td>
<td align="left" width="63%">
Sets the current visibility and enabled states of a given control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e235e82e-65db-4919-bf71-c454673d07fb">SetEditBoxText</a>
</td>
<td align="left" width="63%">
Sets the text in an edit box control found in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff0287db-fdd8-415c-9c78-607ec79b5e2d">SetSelectedControlItem</a>
</td>
<td align="left" width="63%">
Sets the selected state of a particular item in an option button group or a combo box found in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2626c820-3731-474d-9ddb-d2a8966c3d35">StartVisualGroup</a>
</td>
<td align="left" width="63%">
Declares a visual group in the dialog. Subsequent calls to any "add" method add those elements to this group.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>

<a href="https://msdn.microsoft.com/745ee176-53bc-4388-beaa-a0856a438ee6">IFileDialogControlEvents</a> is implemented on the file dialog object.

Controls are added to the dialog before the dialog is shown. Their layout is implied by the order in which they are added. Once the dialog is shown, controls cannot be added or removed, but the existing controls can be hidden or disabled at any time. Their labels can also be changed at any time.

Container controls are controls that can have items added to them. Container controls include combo boxes, menus, the drop-down list attached to the <b>Open</b> button, and any option button groups. The order that items appear in a container is the order in which they were added. There is no facility for reordering them. IDs are scoped to the parent control. Container controls, with the exception of menus, have a selected item.

Items with a container control cannot be changed after they have been created, except for their enabled and visible states. However, they can be added and removed at any time. For example, if you needed to change the text of a menu, you would have to remove the current menu and add another with the correct text.




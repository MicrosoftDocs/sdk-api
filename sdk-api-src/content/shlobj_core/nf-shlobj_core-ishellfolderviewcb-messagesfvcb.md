---
UID: NF:shlobj_core.IShellFolderViewCB.MessageSFVCB
title: IShellFolderViewCB::MessageSFVCB (shlobj_core.h)
author: windows-sdk-content
description: Allows communication between the system folder view object and a system folder view callback object.
old-location: shell\IShellFolderViewCB_MessageSFVCB.htm
tech.root: shell
ms.assetid: 1678dd76-6ed4-4625-9170-22dcd3d7e8d2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellFolderViewCB interface [Windows Shell],MessageSFVCB method, IShellFolderViewCB.MessageSFVCB, IShellFolderViewCB::MessageSFVCB, MessageSFVCB, MessageSFVCB method [Windows Shell], MessageSFVCB method [Windows Shell],IShellFolderViewCB interface, _win32_IShellFolderViewCB_MessageSFVCB, shell.IShellFolderViewCB_MessageSFVCB, shlobj_core/IShellFolderViewCB::MessageSFVCB
ms.topic: method
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
req.lib: 
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
 - IShellFolderViewCB.MessageSFVCB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellFolderViewCB::MessageSFVCB


## -description


Allows communication between the system folder view object and a system folder view callback object.


## -parameters




### -param uMsg [in]

Type: <b>UINT</b>

One of the following notifications.
					
				

<table class="clsStd">
<tr>
<th>Notification</th>
<th>Usage</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/54f67d0e-6089-4e75-a547-5313794e1512">SFVM_ADDPROPERTYPAGES</a>
</td>
<td>Allows the callback object to provide a page to add to the <b>Properties</b> property sheet of the selected object.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8428179c-2ec9-4979-9281-c2439e58beb6">SFVM_BACKGROUNDENUM</a>
</td>
<td>Allows the callback object to request that enumeration be done on a background thread.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/31cba726-c52f-46ba-8852-5dca9756206a">SFVM_BACKGROUNDENUMDONE</a>
</td>
<td>Notifies the callback object that background enumeration is complete.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/351be842-6ea5-4223-8162-0e6c4e6a5afb">SFVM_COLUMNCLICK</a>
</td>
<td>Notifies the callback object that the user has clicked a column header to sort the list of objects in the folder view.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/62306eaa-e52e-432b-9233-d990519d5739">SFVM_DEFITEMCOUNT</a>
</td>
<td>Allows the callback object to specify the number of items in the folder view.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/5118fc81-490f-4d76-9361-0d6af0c4b4c0">SFVM_DEFVIEWMODE</a>
</td>
<td>Allows the callback object to specify the view mode.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/5d37cf61-d8a7-4afa-9159-fea13d2b1d59">SFVM_DIDDRAGDROP</a>
</td>
<td>Notifies the callback function that a drag-and-drop operation has begun.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/ff159c35-afdf-4147-8dd6-7febd9519b18">SFVM_FSNOTIFY</a>
</td>
<td>Notifies the callback object that an event has taken place that affects one of its items.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/6f8b3894-f08f-4ebf-a645-87869e7d1b20">SFVM_GETANIMATION</a>
</td>
<td>Allows the callback object to specify that an animation be displayed while items are enumerated on a background thread.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/983652ed-7309-46aa-a6c9-7516411ba5ac">SFVM_GETBUTTONINFO</a>
</td>
<td>Allows the callback object to add buttons to the toolbar.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/0c0dbf61-9da9-4bcc-bad9-92c3f78db78f">SFVM_GETBUTTONS</a>
</td>
<td>Allows the callback object to specify the buttons to be added to the toolbar.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/46a81a7b-527c-4d41-8d25-ce65fd87416e">SFVM_GETDETAILSOF</a>
</td>
<td>Allows the callback object to provide the details for an item in a Shell folder. Use only if a call to <a href="https://msdn.microsoft.com/bd9e8b6c-ed70-455e-8316-ac0868493802">GetDetailsOf</a> fails and there is no <a href="https://msdn.microsoft.com/5442dc80-9ecf-4e47-a84d-6da4327696ef">GetDetailsOf</a> method available to call.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/9bd6d632-308c-4ba5-8ac6-2d0f65853947">SFVM_GETHELPTEXT</a>
</td>
<td>Allows the callback object to specify a help text string for menu items or toolbar buttons.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/bbe92e9f-4074-4101-a945-072866ab20a8">SFVM_GETHELPTOPIC</a>
</td>
<td>Allows the callback object to specify a Help file and topic.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/87933217-dfa9-4aaf-9630-fa2c302b18fa">SFVM_GETNOTIFY</a>
</td>
<td>Specifies which events will generate an <a href="https://msdn.microsoft.com/ff159c35-afdf-4147-8dd6-7febd9519b18">SFVM_FSNOTIFY</a> message for a given item.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/9621b921-e97f-4219-953a-7c961a81c379">SFVM_GETPANE</a>
</td>
<td>Allows the callback object to provide the status bar pane in which to display the Internet zone information.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/edd428f2-50d9-4819-ba77-df51262e33ff">SFVM_GETSORTDEFAULTS</a>
</td>
<td>Allows the callback object to specify default sorting parameters.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/29849218-0d30-4412-86c8-5d320bc5dd26">SFVM_GETTOOLTIPTEXT</a>
</td>
<td>Allows the callback object to specify a <a href="https://msdn.microsoft.com/en-us/library/Bb760250(v=VS.85).aspx">tooltip</a> text string for menu items or toolbar buttons.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/6fae7925-b1be-4270-9318-7fa517563dad">SFVM_GETZONE</a>
</td>
<td>Allows the callback object to provide Internet zone information.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/9d7e96e9-c52e-43bd-945b-05db33c8dfd0">SFVM_INITMENUPOPUP</a>
</td>
<td>Allows the callback object to modify an item's context menu.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/6b9e4a4d-ec45-489c-bbff-d123d5756b75">SFVM_INVOKECOMMAND</a>
</td>
<td>Notifies the callback object that one of its toolbar or menu commands has been invoked.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/59bb99a3-9a5a-4ea5-9830-b04d7d886b3f">SFVM_MERGEMENU</a>
</td>
<td>Allows the callback object to merge menu items into the Windows Explorer menus.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/5d777115-bae3-47c4-9edc-c99c40a4f926">SFVM_QUERYFSNOTIFY</a>
</td>
<td>Allows the callback object to register a folder so that changes to that folder's view will generate notifications.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/a4aa40f8-1d98-4686-86e2-87280e470aac">SFVM_SETISFV</a>
</td>
<td>Notifies the callback object of the container site. This is used only when <a href="https://msdn.microsoft.com/5e95b2a6-85b3-4899-9e23-54ed9e69e821">IObjectWithSite::SetSite</a> is not supported and <a href="https://msdn.microsoft.com/7edd6786-7d74-4065-8cf1-cbb489007a46">SHCreateShellFolderViewEx</a> is used.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/43c61d5e-715a-4463-971b-31fd346ed5c4">SFVM_SIZE</a>
</td>
<td>Notifies the callback object that the folder view has been resized.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/488f696d-aa71-4727-bbd2-c99e7d245d85">SFVM_THISIDLIST</a>
</td>
<td>Allows the callback object to specify the view's PIDL. This is used only when <a href="https://msdn.microsoft.com/0f509a36-e9be-46ab-8c01-067e44379615">SetIDList</a> and <a href="https://msdn.microsoft.com/6aaf6ed5-ae8e-4521-80cb-ec45af8827aa">IPersistFolder2::GetCurFolder</a> have failed.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/0255a41d-e8b4-48d2-931a-aa76ad83c18c">SFVM_UNMERGEMENU</a>
</td>
<td>Notifies the callback object that a menu is being removed.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f1bac364-1011-4308-8b9b-8ed1800dd30d">SFVM_UPDATESTATUSBAR</a>
</td>
<td>Allows the callback object to request that the status bar be updated.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b57eb1d8-a897-4358-a855-89e152035eff">SFVM_WINDOWCREATED</a>
</td>
<td>Notifies the callback object that the folder view window is being created.</td>
</tr>
</table>
 


### -param wParam

Type: <b>WPARAM</b>

Additional information. See the individual notification pages for specific requirements.


### -param lParam

Type: <b>LPARAM</b>

Additional information. See the individual notification pages for specific requirements.


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The notification has been handled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The message has not been handled and the system folder view object should perform default processing.

</td>
</tr>
</table>
 




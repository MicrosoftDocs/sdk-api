---
UID: NF:shlobj_core.SHChangeNotify
title: SHChangeNotify function (shlobj_core.h)
description: Notifies the system of an event that an application has performed. An application should use this function if it performs an action that may affect the Shell.
helpviewer_keywords: ["SHCNE_ALLEVENTS","SHCNE_ASSOCCHANGED","SHCNE_ATTRIBUTES","SHCNE_CREATE","SHCNE_DELETE","SHCNE_DISKEVENTS","SHCNE_DRIVEADD","SHCNE_DRIVEADDGUI","SHCNE_DRIVEREMOVED","SHCNE_EXTENDED_EVENT","SHCNE_FREESPACE","SHCNE_GLOBALEVENTS","SHCNE_INTERRUPT","SHCNE_MEDIAINSERTED","SHCNE_MEDIAREMOVED","SHCNE_MKDIR","SHCNE_NETSHARE","SHCNE_NETUNSHARE","SHCNE_RENAMEFOLDER","SHCNE_RENAMEITEM","SHCNE_RMDIR","SHCNE_SERVERDISCONNECT","SHCNE_UPDATEDIR","SHCNE_UPDATEIMAGE","SHCNE_UPDATEITEM","SHCNF_DWORD","SHCNF_FLUSH","SHCNF_FLUSHNOWAIT","SHCNF_IDLIST","SHCNF_NOTIFYRECURSIVE","SHCNF_PATH","SHCNF_PRINTER","SHChangeNotify","SHChangeNotify function [Windows Shell]","_win32_SHChangeNotify","shell.SHChangeNotify","shlobj_core/SHChangeNotify"]
old-location: shell\SHChangeNotify.htm
tech.root: shell
ms.assetid: a9222ce9-0d06-4fd0-af3a-fd0e979713ce
ms.date: 12/05/2018
ms.keywords: SHCNE_ALLEVENTS, SHCNE_ASSOCCHANGED, SHCNE_ATTRIBUTES, SHCNE_CREATE, SHCNE_DELETE, SHCNE_DISKEVENTS, SHCNE_DRIVEADD, SHCNE_DRIVEADDGUI, SHCNE_DRIVEREMOVED, SHCNE_EXTENDED_EVENT, SHCNE_FREESPACE, SHCNE_GLOBALEVENTS, SHCNE_INTERRUPT, SHCNE_MEDIAINSERTED, SHCNE_MEDIAREMOVED, SHCNE_MKDIR, SHCNE_NETSHARE, SHCNE_NETUNSHARE, SHCNE_RENAMEFOLDER, SHCNE_RENAMEITEM, SHCNE_RMDIR, SHCNE_SERVERDISCONNECT, SHCNE_UPDATEDIR, SHCNE_UPDATEIMAGE, SHCNE_UPDATEITEM, SHCNF_DWORD, SHCNF_FLUSH, SHCNF_FLUSHNOWAIT, SHCNF_IDLIST, SHCNF_NOTIFYRECURSIVE, SHCNF_PATH, SHCNF_PRINTER, SHChangeNotify, SHChangeNotify function [Windows Shell], _win32_SHChangeNotify, shell.SHChangeNotify, shlobj_core/SHChangeNotify
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHChangeNotify
 - shlobj_core/SHChangeNotify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - api-ms-win-shell-changenotify-l1-1-1.dll
 - Shell32.dll
 - API-MS-Win-Shell-Changenotify-L1-1-0.dll
 - Ext-Ms-Win-Shell-Directory-L1-1-0.dll
 - Ext-MS-Win-Shell-Shell32-L1-1-0.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-0.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - Windows.Storage.dll
api_name:
 - SHChangeNotify
req.apiset: ext-ms-win-shell-shell32-l1-2-0 (introduced in Windows 8.1)
---

# SHChangeNotify function


## -description

Notifies the system of an event that an application has performed. An application should use this function if it performs an action that may affect the Shell.

## -parameters

### -param wEventId

Type: <b>LONG</b>

Describes the event that has occurred. Typically, only one event is specified at a time. If more than one event is specified, the values contained in the <i>dwItem1</i> and <i>dwItem2</i> parameters must be the same, respectively, for all specified events. This parameter can be one or more of the following values:





#### SHCNE_ALLEVENTS

All events have occurred.



#### SHCNE_ASSOCCHANGED

A file type association has changed. <b>SHCNF_IDLIST</b> must be specified in the <i>uFlags</i> parameter. <i>dwItem1</i> and <i>dwItem2</i> are not used and must be <b>NULL</b>. This event should also be sent for registered protocols.



#### SHCNE_ATTRIBUTES

The attributes of an item or folder have changed. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the item or folder that has changed. <i>dwItem2</i> is not used and should be <b>NULL</b>.



#### SHCNE_CREATE

A nonfolder item has been created. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the item that was created. <i>dwItem2</i> is not used and should be <b>NULL</b>.



#### SHCNE_DELETE

A nonfolder item has been deleted. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the item that was deleted. <i>dwItem2</i> is not used and should be <b>NULL</b>.



#### SHCNE_DRIVEADD

A drive has been added. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the root of the drive that was added. <i>dwItem2</i> is not used and should be <b>NULL</b>.



#### SHCNE_DRIVEADDGUI

<b>Windows XP and later</b>: Not used.



#### SHCNE_DRIVEREMOVED

A drive has been removed. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the root of the drive that was removed. <i>dwItem2</i> is not used and should be <b>NULL</b>.



#### SHCNE_EXTENDED_EVENT

Not currently used.



#### SHCNE_FREESPACE

The amount of free space on a drive has changed. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the root of the drive on which the free space changed. <i>dwItem2</i> is not used and should be <b>NULL</b>.



#### SHCNE_MEDIAINSERTED

Storage media has been inserted into a drive. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the root of the drive that contains the new media. <i>dwItem2</i> is not used and should be <b>NULL</b>.



#### SHCNE_MEDIAREMOVED

Storage media has been removed from a drive. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the root of the drive from which the media was removed. <i>dwItem2</i> is not used and should be <b>NULL</b>.



#### SHCNE_MKDIR

A folder has been created. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the folder that was created. <i>dwItem2</i> is not used and should be <b>NULL</b>.



#### SHCNE_NETSHARE

A folder on the local computer is being shared via the network. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the folder that is being shared. <i>dwItem2</i> is not used and should be <b>NULL</b>.



#### SHCNE_NETUNSHARE

A folder on the local computer is no longer being shared via the network. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the folder that is no longer being shared. <i>dwItem2</i> is not used and should be <b>NULL</b>.



#### SHCNE_RENAMEFOLDER

The name of a folder has changed. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the previous PIDL or name of the folder. <i>dwItem2</i> contains the new PIDL or name of the folder.



#### SHCNE_RENAMEITEM

The name of a nonfolder item has changed. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the previous PIDL or name of the item. <i>dwItem2</i> contains the new PIDL or name of the item.



#### SHCNE_RMDIR

A folder has been removed. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the folder that was removed. <i>dwItem2</i> is not used and should be <b>NULL</b>.



#### SHCNE_SERVERDISCONNECT

The computer has disconnected from a server. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the server from which the computer was disconnected. <i>dwItem2</i> is not used and should be <b>NULL</b>.



#### SHCNE_UPDATEDIR

The contents of an existing folder have changed, but the folder still exists and has not been renamed. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the folder that has changed. <i>dwItem2</i> is not used and should be <b>NULL</b>. If a folder has been created, deleted, or renamed, use <b>SHCNE_MKDIR</b>, <b>SHCNE_RMDIR</b>, or <b>SHCNE_RENAMEFOLDER</b>, respectively.



#### SHCNE_UPDATEIMAGE

An image in the system image list has changed. <b>SHCNF_DWORD</b> must be specified in <i>uFlags</i>.

<i>dwItem2</i> contains the index in the system image list that has changed. <i>dwItem1</i> is not used and should be <b>NULL</b>.



#### SHCNE_UPDATEITEM

An existing item (a folder or a nonfolder) has changed, but the item still exists and has not been renamed. <b>SHCNF_IDLIST</b> or <b>SHCNF_PATH</b> must be specified in <i>uFlags</i>. <i>dwItem1</i> contains the item that has changed. <i>dwItem2</i> is not used and should be <b>NULL</b>. If a nonfolder item has been created, deleted, or renamed, use <b>SHCNE_CREATE</b>, <b>SHCNE_DELETE</b>, or <b>SHCNE_RENAMEITEM</b>, respectively, instead.



#### SHCNE_DISKEVENTS

Specifies a combination of all of the disk event identifiers.



#### SHCNE_GLOBALEVENTS

Specifies a combination of all of the global event identifiers.



#### SHCNE_INTERRUPT

The specified event occurred as a result of a system interrupt. As this value modifies other event values, it cannot be used alone.

### -param uFlags

Type: <b>UINT</b>

Flags that, when combined bitwise with <b>SHCNF_TYPE</b>, indicate the meaning of the <i>dwItem1</i> and <i>dwItem2</i> parameters. The <i>uFlags</i> parameter must be one of the following values.



#### SHCNF_DWORD

The <i>dwItem1</i> and <i>dwItem2</i> parameters are <b>DWORD</b> values.



#### SHCNF_IDLIST

<i>dwItem1</i> and <i>dwItem2</i> are the addresses of <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structures that represent the item(s) affected by the change. Each <b>ITEMIDLIST</b> must be relative to the desktop folder.



#### SHCNF_PATH

<i>dwItem1</i> and <i>dwItem2</i> are the addresses of null-terminated strings of maximum length <b>MAX_PATH</b> that contain the full path names of the items affected by the change.



#### SHCNF_PRINTER

<i>dwItem1</i> and <i>dwItem2</i> are the addresses of null-terminated strings that represent the friendly names of the printer(s) affected by the change.



#### SHCNF_FLUSH

The function should not return until the notification has been delivered to all affected components. As this flag modifies other data-type flags, it cannot be used by itself.



#### SHCNF_FLUSHNOWAIT

The function should begin delivering notifications to all affected components but should return as soon as the notification process has begun. As this flag modifies other data-type flags, it cannot by used by itself. This flag includes <b>SHCNF_FLUSH</b>.



#### SHCNF_NOTIFYRECURSIVE

Notify clients registered for all children.

### -param dwItem1 [in, optional]

Type: <b>LPCVOID</b>

Optional. First event-dependent value.

### -param dwItem2 [in, optional]

Type: <b>LPCVOID</b>

Optional. Second event-dependent value.

## -remarks

Applications that register new handlers of any type must call <b>SHChangeNotify</b> with the <b>SHCNE_ASSOCCHANGED</b> flag to instruct the Shell to invalidate the icon and thumbnail cache. This will also load new icon and thumbnail handlers that have been registered. Note, however, that icon overlay handlers are not reloaded.

The strings pointed to by <i>dwItem1</i> and <i>dwItem2</i> can be either ANSI or Unicode.

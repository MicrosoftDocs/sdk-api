---
UID: NF:shlobj_core.IShellChangeNotify.OnChange
title: IShellChangeNotify::OnChange (shlobj_core.h)
description: Informs a namespace extension that an event has taken place that affects its items.
helpviewer_keywords: ["IShellChangeNotify interface [Windows Shell]","OnChange method","IShellChangeNotify.OnChange","IShellChangeNotify::OnChange","OnChange","OnChange method [Windows Shell]","OnChange method [Windows Shell]","IShellChangeNotify interface","SHCNE_ALLEVENTS","SHCNE_ASSOCCHANGED","SHCNE_ATTRIBUTES","SHCNE_CREATE","SHCNE_DELETE","SHCNE_DISKEVENTS","SHCNE_DRIVEADD","SHCNE_DRIVEADDGUI","SHCNE_DRIVEREMOVED","SHCNE_FREESPACE","SHCNE_GLOBALEVENTS","SHCNE_INTERRUPT","SHCNE_MEDIAINSERTED","SHCNE_MEDIAREMOVED","SHCNE_MKDIR","SHCNE_NETSHARE","SHCNE_NETUNSHARE","SHCNE_RENAMEFOLDER","SHCNE_RENAMEITEM","SHCNE_RMDIR","SHCNE_SERVERDISCONNECT","SHCNE_UPDATEDIR","SHCNE_UPDATEIMAGE","SHCNE_UPDATEITEM","_win32_IShellChangeNotify_OnChange","shell.IShellChangeNotify_OnChange","shlobj_core/IShellChangeNotify::OnChange"]
old-location: shell\IShellChangeNotify_OnChange.htm
tech.root: shell
ms.assetid: 27ef6a2e-e463-4ba7-922f-20bf8e118d3a
ms.date: 12/05/2018
ms.keywords: IShellChangeNotify interface [Windows Shell],OnChange method, IShellChangeNotify.OnChange, IShellChangeNotify::OnChange, OnChange, OnChange method [Windows Shell], OnChange method [Windows Shell],IShellChangeNotify interface, SHCNE_ALLEVENTS, SHCNE_ASSOCCHANGED, SHCNE_ATTRIBUTES, SHCNE_CREATE, SHCNE_DELETE, SHCNE_DISKEVENTS, SHCNE_DRIVEADD, SHCNE_DRIVEADDGUI, SHCNE_DRIVEREMOVED, SHCNE_FREESPACE, SHCNE_GLOBALEVENTS, SHCNE_INTERRUPT, SHCNE_MEDIAINSERTED, SHCNE_MEDIAREMOVED, SHCNE_MKDIR, SHCNE_NETSHARE, SHCNE_NETUNSHARE, SHCNE_RENAMEFOLDER, SHCNE_RENAMEITEM, SHCNE_RMDIR, SHCNE_SERVERDISCONNECT, SHCNE_UPDATEDIR, SHCNE_UPDATEIMAGE, SHCNE_UPDATEITEM, _win32_IShellChangeNotify_OnChange, shell.IShellChangeNotify_OnChange, shlobj_core/IShellChangeNotify::OnChange
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellChangeNotify::OnChange
 - shlobj_core/IShellChangeNotify::OnChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellChangeNotify.OnChange
---

# IShellChangeNotify::OnChange


## -description

Informs a namespace extension that an event has taken place that affects its items.

## -parameters

### -param lEvent

Type: <b>LONG</b>

A value that describes the event that has occurred. Typically, only one event is specified at a time. If more than one event is specified, the values contained in the <i>pidl1</i> and <i>pidl2</i> parameters must be the same, respectively, for all specified events.The <i>lEvent</i> parameter may contain one or more of the following flags.



#### SHCNE_ALLEVENTS (0x7FFFFFFFL)

All events have occurred.



#### SHCNE_ASSOCCHANGED (0x08000000L)

A file type association has changed. The <i>pidl1</i> and <i>pidl2</i> parameters are not used and must be <b>NULL</b>.



#### SHCNE_ATTRIBUTES (0x00000800L)

The attributes of an item or folder have changed. The <i>pidl1</i> parameter contains the item or folder that has changed. The <i>pidl2</i> parameter is not used and should be <b>NULL</b>.



#### SHCNE_CREATE (0x00000002L)

A nonfolder item has been created. The <i>pidl1</i> parameter contains the item that was created. The <i>pidl2</i> parameter is not used and should be <b>NULL</b>.



#### SHCNE_DELETE (0x00000004L)

A nonfolder item has been deleted. The <i>pidl1</i> parameter contains the item that was deleted. The <i>pidl2</i> parameter is not used and should be <b>NULL</b>.



#### SHCNE_DRIVEADD (0x00000100L)

A drive has been added. The <i>pidl1</i> parameter contains the root of the drive that was added. The <i>pidl2</i> parameter is not used and should be <b>NULL</b>.



#### SHCNE_DRIVEADDGUI (0x00010000L)

<b>Windows XP and later</b>: Not used. 



#### SHCNE_DRIVEREMOVED (0x00000080L)

A drive has been removed. The <i>pidl1</i> parameter contains the root of the drive that was removed. The <i>pidl2</i> parameter is not used and should be <b>NULL</b>.



#### SHCNE_FREESPACE (0x00040000L)

The amount of free space on a drive has changed. The <i>pidl1</i> parameter contains the root of the drive on which the free space changed. The <i>pidl2</i> parameter is not used and should be <b>NULL</b>.



#### SHCNE_MEDIAINSERTED (0x00000020L)

Storage media has been inserted into a drive. The <i>pidl1</i> parameter contains the root of the drive that contains the new media. The <i>pidl2</i> parameter is not used and should be <b>NULL</b>.



#### SHCNE_MEDIAREMOVED (0x00000040L)

Storage media has been removed from a drive. The <i>pidl1</i> parameter contains the root of the drive from which the media was removed. The <i>pidl2</i> parameter is not used and should be <b>NULL</b>.



#### SHCNE_MKDIR (0x00000008L)

A folder has been created. The <i>pidl1</i> parameter contains the folder that was created. The <i>pidl2</i> parameter is not used and should be <b>NULL</b>.



#### SHCNE_NETSHARE (0x00000200L)

A folder on the local computer is being shared through the network. The <i>pidl1</i> parameter contains the folder that is being shared. The <i>pidl2</i> parameter is not used and should be <b>NULL</b>.



#### SHCNE_NETUNSHARE (0x00000400L)

A folder on the local computer is no longer being shared through the network. The <i>pidl1</i> parameter contains the folder that is no longer being shared. The <i>pidl2</i> parameter is not used and should be <b>NULL</b>.



#### SHCNE_RENAMEFOLDER (0x00020000L)

The name of a folder has changed. The <i>pidl1</i> parameter contains the previous PIDL or name of the folder. The <i>pidl2</i> parameter contains the new PIDL or name of the folder.



#### SHCNE_RENAMEITEM (0x00000001L)

The name of a nonfolder item has changed. The <i>pidl1</i> parameter contains the previous PIDL or name of the item. The <i>pidl2</i> parameter contains the new PIDL or name of the item.



#### SHCNE_RMDIR (0x00000010L)

A folder has been removed. The <i>pidl1</i> parameter contains the folder that was removed. The <i>pidl2</i> parameter is not used and should be <b>NULL</b>.



#### SHCNE_SERVERDISCONNECT (0x00004000L)

The computer has disconnected from a server. The <i>pidl1</i> parameter contains the server from which the computer was disconnected. The <i>pidl2</i> parameter is not used and should be <b>NULL</b>.



#### SHCNE_UPDATEDIR (0x00001000L)

The contents of an existing folder have changed, but the folder still exists and has not been renamed. The <i>pidl1</i> parameter contains the folder that has changed. The <i>pidl2</i> parameter is not used and should be <b>NULL</b>. If a folder has been created, deleted, or renamed, use <b>SHCNE_MKDIR</b>, <b>SHCNE_RMDIR</b>, or <b>SHCNE_RENAMEFOLDER</b>, respectively, instead.



#### SHCNE_UPDATEIMAGE (0x00008000L)

An image in the system image list has changed. The <i>pidl2</i> parameter contains the index in the system image list that has changed.



#### SHCNE_UPDATEITEM (0x00002000L)

An existing item (a folder or a nonfolder) has changed, but the item still exists and has not been renamed. The <i>pidl1</i> parameter contains the item that has changed. The <i>pidl2</i> parameter is not used and should be <b>NULL</b>. If a nonfolder item has been created, deleted, or renamed, use <b>SHCNE_CREATE</b>, <b>SHCNE_DELETE</b>, or <b>SHCNE_RENAMEITEM</b>, respectively, instead.

The following values specify combinations of other events.



#### SHCNE_DISKEVENTS (0x0002381FL)

Specifies a combination of all of the disk event identifiers.



#### SHCNE_GLOBALEVENTS (0x0C0581E0L)

Specifies a combination of all of the global event identifiers.

The following value modifies other event values and cannot be used alone.



#### SHCNE_INTERRUPT (0x80000000L)

The specified event occurred as a result of a system interrupt.

### -param pidl1 [in, optional]

Type: <b>PCIDLIST_ABSOLUTE</b>

The first event-dependent item identifier.

### -param pidl2 [in, optional]

Type: <b>PCIDLIST_ABSOLUTE</b>

The second event-dependent item identifier.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is similar in function and usage to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify">SHChangeNotify</a>.
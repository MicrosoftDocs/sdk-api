---
UID: NF:shlobj_core.SHChangeNotifyRegister
title: SHChangeNotifyRegister function (shlobj_core.h)
description: Registers a window to receive notifications from the file system or Shell, if the file system supports notifications.
helpviewer_keywords: ["NTSHChangeNotifyRegister","SHCNRF_InterruptLevel","SHCNRF_NewDelivery","SHCNRF_RecursiveInterrupt","SHCNRF_ShellLevel","SHChangeNotifyRegister","SHChangeNotifyRegister function [Windows Shell]","_win32_SHChangeNotifyRegister","shell.SHChangeNotifyRegister","shlobj_core/NTSHChangeNotifyRegister","shlobj_core/SHChangeNotifyRegister"]
old-location: shell\SHChangeNotifyRegister.htm
tech.root: shell
ms.assetid: 73143865-ca2f-4578-a7a2-2ba4833eddd8
ms.date: 12/05/2018
ms.keywords: NTSHChangeNotifyRegister, SHCNRF_InterruptLevel, SHCNRF_NewDelivery, SHCNRF_RecursiveInterrupt, SHCNRF_ShellLevel, SHChangeNotifyRegister, SHChangeNotifyRegister function [Windows Shell], _win32_SHChangeNotifyRegister, shell.SHChangeNotifyRegister, shlobj_core/NTSHChangeNotifyRegister, shlobj_core/SHChangeNotifyRegister
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHChangeNotifyRegister
 - shlobj_core/SHChangeNotifyRegister
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
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - windows.storage.dll
api_name:
 - SHChangeNotifyRegister
 - NTSHChangeNotifyRegister
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# SHChangeNotifyRegister function


## -description

Registers a window to receive notifications from the file system or Shell, if the file system supports notifications.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window that receives the change or notification messages.

### -param fSources

Type: <b>int</b>

One or more of the following values that indicate the type of events for which to receive notifications.
    
    					

<div class="alert"><b>Note</b>  In earlier versions of the SDK, these flags are not defined in a header file and implementers must define these values themselves or use their numeric values directly. As of Windows Vista, these flags are defined in Shlobj.h.</div>
<div> </div>


#### SHCNRF_InterruptLevel (0x0001)

Interrupt level notifications from the file system.



#### SHCNRF_ShellLevel (0x0002)

Shell-level notifications from the shell.



#### SHCNRF_RecursiveInterrupt (0x1000)

Interrupt events on the whole subtree. This flag must be combined with the <b>SHCNRF_InterruptLevel</b> flag. When using this flag, notifications must also be made recursive by setting the <b>fRecursive</b> member of the corresponding <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangenotifyentry">SHChangeNotifyEntry</a> structure referenced by <i>pshcne</i> to <b>TRUE</b>. Use of <b>SHCNRF_RecursiveInterrupt</b> on a single level view—for example, a PIDL that is relative and contains only one <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a>—will block event notification at the highest level and thereby prevent a recursive, child update. Thus, an icon dragged into the lowest level of a folder hierarchy may fail to appear in the view as expected.



#### SHCNRF_NewDelivery (0x8000)

Messages received use shared memory. Call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_lock">SHChangeNotification_Lock</a> to access the actual data. Call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_unlock">SHChangeNotification_Unlock</a> to release the memory when done.
        
                                

<div class="alert"><b>Note</b>  We recommend this flag because it provides a more robust delivery method. All clients should specify this flag.</div>
<div> </div>

### -param fEvents

Type: <b>LONG</b>

Change notification events for which to receive notification. See the SHCNE flags listed in <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify">SHChangeNotify</a> for possible values.

### -param wMsg

Type: <b>UINT</b>

Message to be posted to the window procedure.

### -param cEntries

Type: <b>int</b>

Number of entries in the <i>pshcne</i> array.

### -param pshcne [in]

Type: <b>const <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangenotifyentry">SHChangeNotifyEntry</a>*</b>

Array of <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangenotifyentry">SHChangeNotifyEntry</a> structures that contain the notifications. This array should always be set to one when calling <b>SHChangeNotifyRegister</b> or <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyderegister">SHChangeNotifyDeregister</a> will not work properly.

## -returns

Type: <b>ULONG</b>

Returns a positive integer registration ID. Returns 0 if out of memory or in response to invalid parameters.

## -remarks

See the <a href="/previous-versions/windows/desktop/legacy/dd940348(v=vs.85)">Change Notify Watcher Sample</a> in the Windows Software Development Kit (SDK) for a full example that demonstrates the use of this function.

When a change notification event is raised, the message indicated by <i>wMsg</i> is delivered to the window specified by the <i>hwnd</i> parameter. 

                

<ul>
<li>If SHCNRF_NewDelivery is specified, the <i>wParam</i> and <i>lParam</i> values in the message should be passed to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_lock">SHChangeNotification_Lock</a> as the <i>hChange</i> and <i>dwProcID</i> parameters respectively.</li>
<li>If SHCNRF_NewDelivery is not specified, <i>wParam</i> is a pointer to two PIDLIST_ABSOLUTE pointers, and <i>lParam</i> specifies the event. The two PIDLIST_ABSOLUTE pointers can be <b>NULL</b>, depending on the event being sent.</li>
</ul>
When a relevant file system event takes place and the <i>hwnd</i> parameter is not <b>NULL</b>, then the message indicated by <i>wMsg</i> is posted to the specified window. Otherwise, if the <i>pshcne</i> parameter is not <b>NULL</b>, then that notification entry is used.

For performance reasons, multiple notifications can be combined into a single notification. For example, if a large number of <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify">SHCNE_UPDATEITEM</a> notifications are generated for files in the same folder, they can be joined into a single <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify">SHCNE_UPDATEDIR</a> notification.

The <b>NTSHChangeNotifyRegister</b> function, which is no longer available as of Windows Vista, was equivalent to <b>SHChangeNotifyRegister</b> with the SHCNRF_NewDelivery flag.

---
UID: NF:winternl.NtNotifyChangeMultipleKeys
title: NtNotifyChangeMultipleKeys function (winternl.h)
description: Requests notification when a registry key or any of its subkeys changes.
helpviewer_keywords: ["NtNotifyChangeMultipleKeys","NtNotifyChangeMultipleKeys function [Windows API]","REG_NOTIFY_CHANGE_ATTRIBUTES","REG_NOTIFY_CHANGE_LAST_SET","REG_NOTIFY_CHANGE_NAME","REG_NOTIFY_CHANGE_SECURITY","base.ntnotifychangemultiplekeys","winprog.ntnotifychangemultiplekeys","winternl/NtNotifyChangeMultipleKeys"]
old-location: winprog\ntnotifychangemultiplekeys.htm
tech.root: winprog
ms.assetid: c1ee9793-490c-45de-a2a5-deab630917f6
ms.date: 04/30/2025
ms.keywords: NtNotifyChangeMultipleKeys, NtNotifyChangeMultipleKeys function [Windows API], REG_NOTIFY_CHANGE_ATTRIBUTES, REG_NOTIFY_CHANGE_LAST_SET, REG_NOTIFY_CHANGE_NAME, REG_NOTIFY_CHANGE_SECURITY, base.ntnotifychangemultiplekeys, winprog.ntnotifychangemultiplekeys, winternl/NtNotifyChangeMultipleKeys
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NtNotifyChangeMultipleKeys
 - winternl/NtNotifyChangeMultipleKeys
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ntdll.dll
api_name:
 - NtNotifyChangeMultipleKeys
---

# NtNotifyChangeMultipleKeys function


## -description

<p class="CCE_Message">[This function may be changed or removed from Windows without further notice. ]

Requests notification when a registry key or any of its subkeys changes.

## -parameters

### -param MasterKeyHandle [in]

A handle to an open key. The handle must be opened with the <b>KEY_NOTIFY</b> access right.

### -param Count [in, optional]

The number of keys objects provided in the <i>SubordinateObjects</i> parameter. This parameter must be 1.

### -param SubordinateObjects [in, optional]

Pointer to an array of <a href="/windows-hardware/drivers/ddi/content/wudfwdm/ns-wudfwdm-_object_attributes">OBJECT_ATTRIBUTES</a> structures, one for each key.   This array can contain one <b>OBJECT_ATTRIBUTES</b> structure and must not be a key in the same hive as the <i>MasterKeyHandle</i> key.

### -param Event [in, optional]

A handle to an event created by the caller. If <i>Event</i> is not <b>NULL</b>, the caller waits until the operation succeeds, at which time the event is signaled.

### -param ApcRoutine [in, optional]

A pointer to an asynchronous procedure call (APC) function supplied by the caller. If <i>ApcRoutine</i> is not <b>NULL</b>, the specified APC function executes after the operation completes. A <a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_work_queue_item">WORK_QUEUE_ITEM</a> must be provided instead of ApcRoutine in the <i>ZwNotifyChangeMultipleKeys</i> variant.

### -param ApcContext [in, optional]

A pointer to a context supplied by the caller for its APC function. This value is passed to the APC function when it is executed. The <i>Asynchronous</i> parameter must be <b>TRUE</b>. If <i>ApcContext</i> is specified, the <i>Event</i> parameter must be <b>NULL</b>. A <a href="/windows-hardware/drivers/ddi/wdm/ne-wdm-_work_queue_type">WORK_QUEUE_TYPE</a> must be provided instead of ApcContext in the <i>ZwNotifyChangeMultipleKeys</i> variant.

### -param IoStatusBlock [out]

A pointer to an <a href="/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_io_status_block">IO_STATUS_BLOCK</a> structure that contains the final status and information about the operation. For successful calls that return data, the number of bytes written to the <i>Buffer</i> parameter is supplied in the <b>Information</b> member of the <b>IO_STATUS_BLOCK</b> structure.

### -param CompletionFilter [in]

A bitmap of operations that trigger notification. This parameter can be one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REG_NOTIFY_CHANGE_NAME_"></a><a id="reg_notify_change_name_"></a><dl>
<dt><b>REG_NOTIFY_CHANGE_NAME </b></dt>
</dl>
</td>
<td width="60%">
Notify the caller if a subkey is added or deleted. 

</td>
</tr>
<tr>
<td width="40%"><a id="REG_NOTIFY_CHANGE_ATTRIBUTES_"></a><a id="reg_notify_change_attributes_"></a><dl>
<dt><b>REG_NOTIFY_CHANGE_ATTRIBUTES </b></dt>
</dl>
</td>
<td width="60%">
Notify the caller of changes to the attributes of the key, such as the security descriptor information. 

</td>
</tr>
<tr>
<td width="40%"><a id="REG_NOTIFY_CHANGE_LAST_SET_"></a><a id="reg_notify_change_last_set_"></a><dl>
<dt><b>REG_NOTIFY_CHANGE_LAST_SET </b></dt>
</dl>
</td>
<td width="60%">
Notify the caller of changes to a value of the key. This can include adding or deleting a value, or changing an existing value. 

</td>
</tr>
<tr>
<td width="40%"><a id="REG_NOTIFY_CHANGE_SECURITY_"></a><a id="reg_notify_change_security_"></a><dl>
<dt><b>REG_NOTIFY_CHANGE_SECURITY </b></dt>
</dl>
</td>
<td width="60%">
Notify the caller of changes to the security descriptor of the key.

</td>
</tr>
</table>

### -param WatchTree [in]

If this parameter is <b>TRUE</b>, the caller is notified about changes to all subkeys of the specified key. If this parameter is <b>FALSE</b>, the caller is notified only about changes to the specified key.

### -param Buffer [out, optional]

Reserved for system use. This parameter must be <b>NULL</b>.

### -param BufferSize [in]

Reserved for system use. This parameter must be zero.

### -param Asynchronous [in]

If this parameter is <b>TRUE</b>, the function returns immediately. If this parameter is <b>FALSE</b>, the function does not return until the specified event occurs.

## -returns

Returns an <b>NTSTATUS</b> or error code.

If the <i>Asynchronous</i> parameter is <b>TRUE</b> and the specified event has not yet occurred, the function returns <b>STATUS_PENDING</b>.

The forms and significance of <b>NTSTATUS</b> error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.

## -remarks

This function has no associated header file. You can also use the <a href="/windows/desktop/DevNotes/-loadlibrary">LoadLibrary</a> and <a href="/windows/desktop/DevNotes/-getprocaddress-">GetProcAddress</a> functions to dynamically link to Ntdll.dll.

## -see-also

<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>

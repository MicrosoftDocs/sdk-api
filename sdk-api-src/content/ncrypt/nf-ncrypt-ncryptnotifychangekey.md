---
UID: NF:ncrypt.NCryptNotifyChangeKey
title: NCryptNotifyChangeKey function (ncrypt.h)
description: Creates or removes a key change notification.
helpviewer_keywords: ["NCRYPT_MACHINE_KEY_FLAG","NCRYPT_REGISTER_NOTIFY_FLAG","NCRYPT_UNREGISTER_NOTIFY_FLAG","NCryptNotifyChangeKey","NCryptNotifyChangeKey function [Security]","ncrypt/NCryptNotifyChangeKey","security.ncryptnotifychangekey"]
old-location: security\ncryptnotifychangekey.htm
tech.root: security
ms.assetid: 2d2ddb55-ef32-4227-b901-ee11e961d0e6
ms.date: 12/05/2018
ms.keywords: NCRYPT_MACHINE_KEY_FLAG, NCRYPT_REGISTER_NOTIFY_FLAG, NCRYPT_UNREGISTER_NOTIFY_FLAG, NCryptNotifyChangeKey, NCryptNotifyChangeKey function [Security], ncrypt/NCryptNotifyChangeKey, security.ncryptnotifychangekey
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptNotifyChangeKey
 - ncrypt/NCryptNotifyChangeKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptNotifyChangeKey
---

# NCryptNotifyChangeKey function


## -description

The <b>NCryptNotifyChangeKey</b> function creates or removes a key change notification.

The handle provided by this function is the same handle that is returned by the <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstchangenotificationa">FindFirstChangeNotification</a> function. You use the <a href="/windows/desktop/Sync/wait-functions">wait functions</a> to wait for the notification handle to be signaled.

## -parameters

### -param hProvider [in]

The handle of the key storage provider. This handle is obtained by using the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenstorageprovider">NCryptOpenStorageProvider</a> function.

### -param phEvent [in, out]

The address of a <b>HANDLE</b> variable that either receives or contains the key change notification event handle. This is the same handle that is returned by the <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstchangenotificationa">FindFirstChangeNotification</a> function. For more information, see the <i>dwFlags</i> parameter description.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. This parameter contains a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_REGISTER_NOTIFY_FLAG"></a><a id="ncrypt_register_notify_flag"></a><dl>
<dt><b>NCRYPT_REGISTER_NOTIFY_FLAG</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Create a new change notification. The <i>phEvent</i> parameter will receive the key change notification handle.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_UNREGISTER_NOTIFY_FLAG"></a><a id="ncrypt_unregister_notify_flag"></a><dl>
<dt><b>NCRYPT_UNREGISTER_NOTIFY_FLAG</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Remove an existing change notification. The <i>phEvent</i> parameter must contain a valid key change notification handle. This handle is no longer valid after this function is called with this flag and the <b>INVALID_HANDLE_VALUE</b> value is placed in this handle.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_MACHINE_KEY_FLAG"></a><a id="ncrypt_machine_key_flag"></a><dl>
<dt><b>NCRYPT_MACHINE_KEY_FLAG</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Receive change notifications for keys in the machine key store. If this flag is not specified, the change notification events will only occur for keys in the calling user's key store. This flag is only valid when combined with the <b>NCRYPT_REGISTER_NOTIFY_FLAG</b> flag.

</td>
</tr>
</table>

## -returns

Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter contains a value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hProvider</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
</table>

## -remarks

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstchangenotificationa">FindFirstChangeNotification</a>
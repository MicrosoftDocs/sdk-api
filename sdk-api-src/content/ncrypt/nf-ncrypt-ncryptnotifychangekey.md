---
UID: NF:ncrypt.NCryptNotifyChangeKey
title: NCryptNotifyChangeKey function
author: windows-sdk-content
description: Creates or removes a key change notification.
old-location: security\ncryptnotifychangekey.htm
tech.root: seccng
ms.assetid: 2d2ddb55-ef32-4227-b901-ee11e961d0e6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NCRYPT_MACHINE_KEY_FLAG, NCRYPT_REGISTER_NOTIFY_FLAG, NCRYPT_UNREGISTER_NOTIFY_FLAG, NCryptNotifyChangeKey, NCryptNotifyChangeKey function [Security], ncrypt/NCryptNotifyChangeKey, security.ncryptnotifychangekey
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptNotifyChangeKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NCryptNotifyChangeKey function


## -description


The <b>NCryptNotifyChangeKey</b> function creates or removes a key change notification.

The handle provided by this function is the same handle that is returned by the <a href="https://msdn.microsoft.com/dde4dd17-0f8c-41b5-8685-4e4c6b3def3c">FindFirstChangeNotification</a> function. You use the <a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a> to wait for the notification handle to be signaled.


## -parameters




### -param hProvider [in]

The handle of the key storage provider. This handle is obtained by using the <a href="https://msdn.microsoft.com/febcf440-78b3-420b-b13d-030e8071cd50">NCryptOpenStorageProvider</a> function.


### -param phEvent [in, out]

The address of a <b>HANDLE</b> variable that either receives or contains the key change notification event handle. This is the same handle that is returned by the <a href="https://msdn.microsoft.com/dde4dd17-0f8c-41b5-8685-4e4c6b3def3c">FindFirstChangeNotification</a> function. For more information, see the <i>dwFlags</i> parameter description.


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



A service must not call this function from its <a href="http://go.microsoft.com/fwlink/p/?linkid=137250">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.




## -see-also




<a href="https://msdn.microsoft.com/dde4dd17-0f8c-41b5-8685-4e4c6b3def3c">FindFirstChangeNotification</a>
 

 


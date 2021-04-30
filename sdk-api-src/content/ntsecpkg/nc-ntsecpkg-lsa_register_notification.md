---
UID: NC:ntsecpkg.LSA_REGISTER_NOTIFICATION
title: LSA_REGISTER_NOTIFICATION (ntsecpkg.h)
description: Provides a mechanism whereby the security package is notified. Notification can occur at fixed intervals, when an event object is signaled, or during certain system events.
helpviewer_keywords: ["LSA_REGISTER_NOTIFICATION","NOTIFIER_FLAG_NEW_THREAD","NOTIFIER_FLAG_ONE_SHOT","NOTIFIER_FLAG_SECONDS","NOTIFIER_TYPE_HANDLE_WAIT","NOTIFIER_TYPE_IMMEDIATE","NOTIFIER_TYPE_INTERVAL","NOTIFIER_TYPE_NOTIFY_EVENT","NOTIFIER_TYPE_STATE_CHANGE","NOTIFY_CLASS_DOMAIN_CHANGE","NOTIFY_CLASS_PACKAGE_CHANGE","NOTIFY_CLASS_ROLE_CHANGE","PLSA_REGISTER_NOTIFICATION callback","RegisterNotification","RegisterNotification callback function [Security]","_ssp_registernotification","ntsecpkg/RegisterNotification","security.registernotification"]
old-location: security\registernotification.htm
tech.root: security
ms.assetid: 689a1956-5eab-4eec-93ef-5ddcef6546ee
ms.date: 12/05/2018
ms.keywords: LSA_REGISTER_NOTIFICATION, NOTIFIER_FLAG_NEW_THREAD, NOTIFIER_FLAG_ONE_SHOT, NOTIFIER_FLAG_SECONDS, NOTIFIER_TYPE_HANDLE_WAIT, NOTIFIER_TYPE_IMMEDIATE, NOTIFIER_TYPE_INTERVAL, NOTIFIER_TYPE_NOTIFY_EVENT, NOTIFIER_TYPE_STATE_CHANGE, NOTIFY_CLASS_DOMAIN_CHANGE, NOTIFY_CLASS_PACKAGE_CHANGE, NOTIFY_CLASS_ROLE_CHANGE, PLSA_REGISTER_NOTIFICATION callback, RegisterNotification, RegisterNotification callback function [Security], _ssp_registernotification, ntsecpkg/RegisterNotification, security.registernotification
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LSA_REGISTER_NOTIFICATION
 - ntsecpkg/LSA_REGISTER_NOTIFICATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - RegisterNotification
---

# LSA_REGISTER_NOTIFICATION callback function


## -description

Provides a mechanism whereby the <a href="/windows/desktop/SecGloss/s-gly">security package</a> is notified. Notification can occur at fixed intervals, when an event object is signaled, or during certain system events.

## -parameters

### -param StartFunction [in]

The function that is called to accept notification.

### -param Parameter [in]

The argument of the function specified in the <i>StartFunction</i> parameter.

### -param NotificationType [in]

Specifies the type of notification. The following table lists the valid values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NOTIFIER_TYPE_INTERVAL"></a><a id="notifier_type_interval"></a><dl>
<dt><b>NOTIFIER_TYPE_INTERVAL</b></dt>
</dl>
</td>
<td width="60%">
Notify at fixed intervals. Use the <i>IntervalMinutes</i> parameter to indicate the interval length.

</td>
</tr>
<tr>
<td width="40%"><a id="NOTIFIER_TYPE_HANDLE_WAIT"></a><a id="notifier_type_handle_wait"></a><dl>
<dt><b>NOTIFIER_TYPE_HANDLE_WAIT</b></dt>
</dl>
</td>
<td width="60%">
Notify when the event handle specified by the <i>WaitEvent</i> parameter is signaled.

</td>
</tr>
<tr>
<td width="40%"><a id="NOTIFIER_TYPE_STATE_CHANGE"></a><a id="notifier_type_state_change"></a><dl>
<dt><b>NOTIFIER_TYPE_STATE_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
Notify when there is a change in the machine's domain or installation type.

</td>
</tr>
<tr>
<td width="40%"><a id="NOTIFIER_TYPE_NOTIFY_EVENT"></a><a id="notifier_type_notify_event"></a><dl>
<dt><b>NOTIFIER_TYPE_NOTIFY_EVENT</b></dt>
</dl>
</td>
<td width="60%">
Notify when a security event takes place. Use the <i>NotificationClass</i> parameter to specify the event of interest.

</td>
</tr>
<tr>
<td width="40%"><a id="NOTIFIER_TYPE_IMMEDIATE"></a><a id="notifier_type_immediate"></a><dl>
<dt><b>NOTIFIER_TYPE_IMMEDIATE</b></dt>
</dl>
</td>
<td width="60%">
Notify immediately. This value implies NOTIFIER_FLAG_ONE_SHOT.

</td>
</tr>
</table>

### -param NotificationClass [in]

Specifies the class of events that generate notifications. Specify zero unless the <i>NotificationType</i> parameter is set to NOTIFIER_TYPE_NOTIFY_EVENT.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NOTIFY_CLASS_PACKAGE_CHANGE"></a><a id="notify_class_package_change"></a><dl>
<dt><b>NOTIFY_CLASS_PACKAGE_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
A package was loaded, or a new package was selected as the preferred package. For more information, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="NOTIFY_CLASS_ROLE_CHANGE"></a><a id="notify_class_role_change"></a><dl>
<dt><b>NOTIFY_CLASS_ROLE_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
Reserved for internal use.

</td>
</tr>
<tr>
<td width="40%"><a id="NOTIFY_CLASS_DOMAIN_CHANGE"></a><a id="notify_class_domain_change"></a><dl>
<dt><b>NOTIFY_CLASS_DOMAIN_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
Reserved for internal use.

</td>
</tr>
</table>

### -param NotificationFlags [in]

Specifies flags that control notification behavior.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NOTIFIER_FLAG_NEW_THREAD"></a><a id="notifier_flag_new_thread"></a><dl>
<dt><b>NOTIFIER_FLAG_NEW_THREAD</b></dt>
</dl>
</td>
<td width="60%">
Wait for notification using a new thread.

</td>
</tr>
<tr>
<td width="40%"><a id="NOTIFIER_FLAG_ONE_SHOT"></a><a id="notifier_flag_one_shot"></a><dl>
<dt><b>NOTIFIER_FLAG_ONE_SHOT</b></dt>
</dl>
</td>
<td width="60%">
Notify only once.

</td>
</tr>
<tr>
<td width="40%"><a id="NOTIFIER_FLAG_SECONDS"></a><a id="notifier_flag_seconds"></a><dl>
<dt><b>NOTIFIER_FLAG_SECONDS</b></dt>
</dl>
</td>
<td width="60%">
The <i>IntervalMinutes</i> parameter specifies seconds.

</td>
</tr>
</table>

### -param IntervalMinutes [in]

Specifies the time delay between notifications.

### -param WaitEvent [in]

Optional. Handle to an event object. When the object is signaled, the notification occurs. This value is used in conjunction with the <i>NotificationType</i> value NOTIFIER_TYPE_HANDLE_WAIT.

## -returns

If the function succeeds, the return value is a handle to the notification.

If the function fails, the return value is <b>NULL</b>.

## -remarks

If you specify the NOTIFY_CLASS_PACKAGE_CHANGE value for the <i>NotificationClass</i> parameter, the following values represent valid changes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>SECPKG_PACKAGE_CHANGE_LOAD</td>
<td>A package was loaded.</td>
</tr>
<tr>
<td>SECPKG_PACKAGE_CHANGE_UNLOAD</td>
<td>A package was unloaded.</td>
</tr>
<tr>
<td>SECPKG_PACKAGE_CHANGE_SELECT</td>
<td>A new package became the preferred <a href="/windows/desktop/SecGloss/s-gly">security package</a>.</td>
</tr>
</table>
 

A pointer to the <b>RegisterNotification</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
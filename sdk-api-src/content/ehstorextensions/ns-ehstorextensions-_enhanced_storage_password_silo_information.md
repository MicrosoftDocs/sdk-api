---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION structure


## -description


The <b>ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION</b> structure contains data that defines the capabilities and requirements of a password silo.


## -struct-fields




### -field CurrentAdminFailures

This is the current number of consecutive unsuccessful authentication attempts using administrator password. This value is reset to 0 after a successful authentication.


### -field CurrentUserFailures

This is the current number of consecutive unsuccessful authentication attempts using user password. This value is reset to 0 after a successful authentication.


### -field TotalUserAuthenticationCount

Total number of authentication attempts attempted on this silo using the user password.


### -field TotalAdminAuthenticationCount

Total number of authentication attempts attempted on this silo using the administrator password.


### -field FipsCompliant

<b>TRUE</b> if the silo claims compliance with the  Federal Information Processing Standard  (FIPS); otherwise, <b>FALSE</b>.


### -field SecurityIDAvailable

<b>TRUE</b> if a device-unique security identifier provided by the manufacturer is available; otherwise, <b>FALSE</b>.


### -field InitializeInProgress

<b>TRUE</b> if an initialization is in progress; otherwise, <b>FALSE</b>.


### -field ITMSArmed

<b>TRUE</b> if the silo is set to prepare for initalization to the default state set by the manufacturer; otherwise, <b>FALSE</b>.


### -field ITMSArmable

<b>TRUE</b> if the silo is capable of initializing to the default state set by the manufacturer; otherwise, <b>FALSE</b>.


### -field UserCreated

<b>TRUE</b> if the user account has been created in the password silo; otherwise, <b>FALSE</b>.


### -field ResetOnPORDefault

<b>TRUE</b> if the silo resets Administrator authentication failure count to zero upon power cycle. This is the default behavior for the silo. 
If <b>FALSE</b>, the silo will not reset Administrator authentication failure count to zero upon power cycle.


### -field ResetOnPORCurrent

<b>TRUE</b> if the silo is currently set to reset Administrator authentication failure count to zero upon power cycle; Otherwise <b>FALSE</b>. 
This configuration is affected by changes introduced by the host or the implementation of factory default settings.


### -field MaxAdminFailures

This is the maximum number of consecutive unsuccessful authentication attempts using administrator password allowed by the silo before it will block the administrator.


### -field MaxUserFailures

This is the maximum number of consecutive unsuccessful authentication attempts using user password allowed by the silo before it will block user.


### -field TimeToCompleteInitialization

Estimated time (in milliseconds) for the device to complete the initialize to manufacturing function.


### -field TimeRemainingToCompleteInitialization

Time remaining (in milliseconds) for the silo to complete the initialize to manufacturing function.  The value of this field is zero if the silo is currently not in the process of initialization.


### -field MinTimeToAuthenticate

Minimum time (in milliseconds) the silo will require to complete an authentication operation.


### -field MaxAdminPasswordSize

This is the maximum number of bytes that the silo supports for administrator password.


### -field MinAdminPasswordSize

This is the minimum number of bytes that the silo requires for administrator password.


### -field MaxAdminHintSize

This is the maximum number of bytes that the silo supports for administrator password hint.


### -field MaxUserPasswordSize

This is the maximum number of bytes that the silo supports for user password.


### -field MinUserPasswordSize

This is the minimum number of bytes that the silo requires for user password.


### -field MaxUserHintSize

This is the maximum number of bytes that the silo supports for user password hint.


### -field MaxUserNameSize

This is the maximum number of bytes that the silo supports for friendly user name.


### -field MaxSiloNameSize

The maximum number of bytes that the silo supports for  the silo name.


### -field MaxChallengeSize

The maximum number of bytes that the device supports for challenge.


## -see-also




<a href="https://msdn.microsoft.com/b848a866-9fdf-4cb3-b289-6df5fc1bf723">Enhanced Storage Portable Device Commands</a>
 

 


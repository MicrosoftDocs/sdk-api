---
UID: NS:ehstorextensions._ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION
title: ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION (ehstorextensions.h)
description: ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION structure contains data that defines the capabilities and requirements of a password silo.
helpviewer_keywords: ["*PENHANCED_STORAGE_PASSWORD_SILO_INFORMATION","ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION","ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION structure [Enhanced Storage]","PENHANCED_STORAGE_PASSWORD_SILO_INFORMATION","PENHANCED_STORAGE_PASSWORD_SILO_INFORMATION structure pointer [Enhanced Storage]","ehstorextensions/ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION","ehstorextensions/PENHANCED_STORAGE_PASSWORD_SILO_INFORMATION","enstor.enhanced_storage_password_silo_information"]
old-location: enstor\enhanced_storage_password_silo_information.htm
tech.root: enstor
ms.assetid: b922aca7-d574-497a-bf83-b53a321400a9
ms.date: 12/05/2018
ms.keywords: '*PENHANCED_STORAGE_PASSWORD_SILO_INFORMATION, ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION, ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION structure [Enhanced Storage], PENHANCED_STORAGE_PASSWORD_SILO_INFORMATION, PENHANCED_STORAGE_PASSWORD_SILO_INFORMATION structure pointer [Enhanced Storage], ehstorextensions/ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION, ehstorextensions/PENHANCED_STORAGE_PASSWORD_SILO_INFORMATION, enstor.enhanced_storage_password_silo_information'
req.header: ehstorextensions.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION, *PENHANCED_STORAGE_PASSWORD_SILO_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION
 - ehstorextensions/_ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION
 - PENHANCED_STORAGE_PASSWORD_SILO_INFORMATION
 - ehstorextensions/PENHANCED_STORAGE_PASSWORD_SILO_INFORMATION
 - ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION
 - ehstorextensions/ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - EhStorExtensions.h
api_name:
 - ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION
---

# ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION structure


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

<b>TRUE</b> if the silo is set to prepare for initialization to the default state set by the manufacturer; otherwise, <b>FALSE</b>.

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

<a href="/previous-versions/windows/desktop/enstor/enhanced-storage-portable-device-commands">Enhanced Storage Portable Device Commands</a>
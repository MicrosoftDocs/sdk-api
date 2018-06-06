---
UID: NS:subauth._USER_ALL_INFORMATION
title: "_USER_ALL_INFORMATION"
author: windows-sdk-content
description: Contains information on the session user.
old-location: security\user_all_information.htm
old-project: SecAuthN
ms.assetid: 18cf7194-4309-47b6-bfd1-9fb52bfddd56
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PUSER_ALL_INFORMATION, PUSER_ALL_INFORMATION, PUSER_ALL_INFORMATION structure pointer [Security], USER_ALL_INFORMATION, USER_ALL_INFORMATION structure [Security], _USER_ALL_INFORMATION, _lsa_user_all_information, security.user_all_information, subauth/PUSER_ALL_INFORMATION, subauth/USER_ALL_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: subauth.h
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
tech.root: 
req.typenames: USER_ALL_INFORMATION, *PUSER_ALL_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Subauth.h
api_name:
 - USER_ALL_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _USER_ALL_INFORMATION structure


## -description


The <b>USER_ALL_INFORMATION</b> structure contains information on the session user.

It is used with subauthentication functions.


## -struct-fields




### -field LastLogon

Indicates the date and time of the last logon.


### -field LastLogoff

Indicates the date and time of the last logoff.


### -field PasswordLastSet

Indicates the date and time when the password was set or last changed.


### -field AccountExpires

Indicates the date and time when the account will expire.


### -field PasswordCanChange

Indicates the date and time when the password can be changed.


### -field PasswordMustChange

Indicates the date and time when the password must change.


### -field UserName

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the name of the user account.


### -field FullName

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the full name of the user or account.


### -field HomeDirectory

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the home directory of the user.


### -field HomeDirectoryDrive

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the home drive name.


### -field ScriptPath

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the path to any logon script.


### -field ProfilePath

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the path to the user's profile.


### -field AdminComment

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing a comment associated with the user account. This string can be a null string, or it can have any number of characters before the terminating null character.


### -field WorkStations

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the name of the workstation in use by the account.


### -field UserComment

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing a user comment. This string can be a null string, or it can have any number of characters before the terminating null character.


### -field Parameters

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> reserved for use by applications. This string can be a null string, or it can have any number of characters before the terminating null character. Microsoft products use this member to store user configuration information. Do not modify this information.


### -field LmPassword

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the user's local machine password.


### -field NtPassword

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing a hash of the user's Windows domain password.


### -field PrivateData

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing supplemental private data associated with the user account. If <b>PrivateDataSensitive</b> is <b>TRUE</b>, this data is encrypted.


### -field SecurityDescriptor


<a href="https://msdn.microsoft.com/000ffbbe-5750-449b-8237-27c8d3c45454">SR_SECURITY_DESCRIPTOR</a> indicating the security <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">privileges</a> of the account.


### -field UserId

Contains the user ID from the account relative identifier (RID). This ID is used by the posix subsystem.


### -field PrimaryGroupId

Indicates the account's primary group. This ID is used by the posix subsystem.


### -field UserAccountControl

Contains flags defined in Subauth.h.


### -field WhichFields

Contains flags defined in Subauth.h.


### -field LogonHours

Indicates the hours when the user can logon.


### -field BadPasswordCount

Indicates the number of times the user tried to log on to this account using an incorrect password.


### -field LogonCount

Indicates the number of logons by the user.


### -field CountryCode

Used for localization. If not equal to zero, value is the country/region code for the user's language of choice.


### -field CodePage

Used for localization. If not equal to zero, the value is the code page for the user's language of choice.


### -field LmPasswordPresent

Indicates whether there is a local machine password.


### -field NtPasswordPresent

Indicates whether there is a Windows domain password.


### -field PasswordExpired

Indicates whether the password has expired.


### -field PrivateDataSensitive

When set to <b>TRUE</b>, indicates that the <b>PrivateData</b> member is encrypted. A value of <b>FALSE</b> indicates that the <b>PrivateData</b> is in <a href="https://msdn.microsoft.com/library/windows/hardware/dn965962">plaintext</a>.


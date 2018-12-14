---
UID: NE:iads.ADS_USER_FLAG
title: ADS_USER_FLAG_ENUM
author: windows-sdk-content
description: Defines the flags used for setting user properties in the directory.
old-location: adsi\ads_user_flag_enum.htm
tech.root: adsi
ms.assetid: c385ef3d-9de4-4938-9733-ad8fe90fb2dc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ADS_UF_ACCOUNTDISABLE, ADS_UF_DONT_EXPIRE_PASSWD, ADS_UF_DONT_REQUIRE_PREAUTH, ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED, ADS_UF_HOMEDIR_REQUIRED, ADS_UF_INTERDOMAIN_TRUST_ACCOUNT, ADS_UF_LOCKOUT, ADS_UF_MNS_LOGON_ACCOUNT, ADS_UF_NORMAL_ACCOUNT, ADS_UF_NOT_DELEGATED, ADS_UF_PASSWD_CANT_CHANGE, ADS_UF_PASSWD_NOTREQD, ADS_UF_PASSWORD_EXPIRED, ADS_UF_SCRIPT, ADS_UF_SERVER_TRUST_ACCOUNT, ADS_UF_SMARTCARD_REQUIRED, ADS_UF_TEMP_DUPLICATE_ACCOUNT, ADS_UF_TRUSTED_FOR_DELEGATION, ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION, ADS_UF_USE_DES_KEY_ONLY, ADS_UF_WORKSTATION_TRUST_ACCOUNT, ADS_USER_FLAG_ENUM, ADS_USER_FLAG_ENUM enumeration [ADSI], _ds_ads_user_flag_enum, adsi.ads__user__flag__enum, adsi.ads_user_flag_enum, iads/ADS_UF_ACCOUNTDISABLE, iads/ADS_UF_DONT_EXPIRE_PASSWD, iads/ADS_UF_DONT_REQUIRE_PREAUTH, iads/ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED, iads/ADS_UF_HOMEDIR_REQUIRED, iads/ADS_UF_INTERDOMAIN_TRUST_ACCOUNT, iads/ADS_UF_LOCKOUT, iads/ADS_UF_MNS_LOGON_ACCOUNT, iads/ADS_UF_NORMAL_ACCOUNT, iads/ADS_UF_NOT_DELEGATED, iads/ADS_UF_PASSWD_CANT_CHANGE, iads/ADS_UF_PASSWD_NOTREQD, iads/ADS_UF_PASSWORD_EXPIRED, iads/ADS_UF_SCRIPT, iads/ADS_UF_SERVER_TRUST_ACCOUNT, iads/ADS_UF_SMARTCARD_REQUIRED, iads/ADS_UF_TEMP_DUPLICATE_ACCOUNT, iads/ADS_UF_TRUSTED_FOR_DELEGATION, iads/ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION, iads/ADS_UF_USE_DES_KEY_ONLY, iads/ADS_UF_WORKSTATION_TRUST_ACCOUNT, iads/ADS_USER_FLAG_ENUM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_USER_FLAG_ENUM
product: Windows
targetos: Windows
req.typenames: ADS_USER_FLAG_ENUM
req.redist: 
---

# ADS_USER_FLAG_ENUM enumeration


## -description


The <b>ADS_USER_FLAG_ENUM</b> enumeration 
   defines the flags used for setting user properties in the directory. These flags correspond to 
   values of the <b>userAccountControl</b> attribute in Active Directory when using the LDAP 
   provider, and the <b>userFlags</b> attribute when using the WinNT system provider.


## -enum-fields




### -field ADS_UF_SCRIPT

The logon script is executed. This flag does not work for the ADSI LDAP provider on either read or write 
      operations. For the  ADSI WinNT provider, this flag is  read-only data, and it cannot be set for user 
      objects.


### -field ADS_UF_ACCOUNTDISABLE

The user account is disabled.


### -field ADS_UF_HOMEDIR_REQUIRED

The home directory is required.


### -field ADS_UF_LOCKOUT

The account is currently locked out.


### -field ADS_UF_PASSWD_NOTREQD

No password is required.


### -field ADS_UF_PASSWD_CANT_CHANGE

The user cannot change the password. This flag can be read, but not set directly.  For more information and 
      a code example that shows how to prevent a user from changing the password, see 
      <a href="https://msdn.microsoft.com/4cd1113d-7e0a-4518-be08-1d2630ee9f7f">User Cannot Change Password</a>.


### -field ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED

The user can send an encrypted password.


### -field ADS_UF_TEMP_DUPLICATE_ACCOUNT

This is an account for users whose primary account is in another domain. This account provides user access 
      to this domain, but not to any domain that trusts this domain. Also known as a  local user account.


### -field ADS_UF_NORMAL_ACCOUNT

This is a default account type that represents a typical user.


### -field ADS_UF_INTERDOMAIN_TRUST_ACCOUNT

This is a permit to trust account for a system domain that trusts other domains.


### -field ADS_UF_WORKSTATION_TRUST_ACCOUNT

This is a computer account for a Windows or Windows Server that is a member of this domain.


### -field ADS_UF_SERVER_TRUST_ACCOUNT

This is a computer account for a system backup domain controller that is a member of this domain.


### -field ADS_UF_DONT_EXPIRE_PASSWD

When set, the password will not expire on this account.


### -field ADS_UF_MNS_LOGON_ACCOUNT

This is an Majority Node Set (MNS) logon account. With MNS, you can configure a multi-node Windows cluster 
      without using a common shared disk.


### -field ADS_UF_SMARTCARD_REQUIRED

When set, this flag will force the user to log on using a smart card.


### -field ADS_UF_TRUSTED_FOR_DELEGATION

When set, the service account (user or computer account), under which a service runs, is trusted for 
      Kerberos delegation. Any such service can impersonate a client requesting the service. To enable a service for 
      Kerberos delegation, set this flag on the  <b>userAccountControl</b> property of the 
      service account.


### -field ADS_UF_NOT_DELEGATED

When set, the security context of the user will not be delegated to a service even if the service account 
      is set as trusted for Kerberos delegation.


### -field ADS_UF_USE_DES_KEY_ONLY

Restrict this principal to use only Data Encryption Standard (DES) encryption types for keys.


### -field ADS_UF_DONT_REQUIRE_PREAUTH

This account does not require Kerberos preauthentication for logon.


### -field ADS_UF_PASSWORD_EXPIRED

The user password has expired. This flag is created by the system using data from the  password last set 
      attribute and the domain policy.  It is read-only and cannot be set. To manually set a user password as expired, 
      use the <a href="https://msdn.microsoft.com/ffe49d4b-e7e8-4982-8087-59bb7534b257">NetUserSetInfo</a> function with the 
      <a href="https://msdn.microsoft.com/39ed05f5-165d-4cb8-98af-e4120a1634f6">USER_INFO_3</a> 
      (<b>usri3_password_expired</b> member) or 
      <a href="https://msdn.microsoft.com/66b11a5f-1c2d-4564-8845-9e2fa1f40f3e">USER_INFO_4</a> 
      (<b>usri4_password_expired</b> member) structure.


### -field ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION

The account is enabled for delegation. This is a security-sensitive setting; accounts with this option 
      enabled should be strictly controlled. This setting enables a service running under the account to assume a 
      client identity and authenticate as that user to other remote servers on the network.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/57c83e4d-2d9f-4f22-97e2-27e2d277f014">Managing Users</a>.

For more information, and a code example that shows how to set the 
     <b>ADS_UF_DONT_EXPIRE_PASSWD</b> value on a user 
     <b>userAccountControl</b> attribute, see 
     <a href="https://msdn.microsoft.com/b8d7e7fe-c846-45c4-9c5f-770530453836">Password Never Expires</a>.

<div class="alert"><b>Note</b>  Because VBScript cannot read data from a type library, VBScript applications do not understand the symbolic 
    constants as defined above. Use the numerical constants, instead, to set the appropriate flags in your VBScript 
    applications. To use the symbolic constants as a good programming practice, create explicit declarations of such 
    constants, as done here, in your VBScript applications.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>



<a href="https://msdn.microsoft.com/57c83e4d-2d9f-4f22-97e2-27e2d277f014">Managing Users</a>



<a href="https://msdn.microsoft.com/5bd13bed-938a-4273-840e-99fca99f7139">NetUserGetInfo</a>
 

 


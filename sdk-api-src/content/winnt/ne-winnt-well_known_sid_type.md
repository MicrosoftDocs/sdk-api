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

# WELL_KNOWN_SID_TYPE enumeration


## -description



			The <b>WELL_KNOWN_SID_TYPE</b> enumeration is a list of commonly used <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs). Programs can pass these values to the <a href="https://msdn.microsoft.com/00e75bae-fbce-41a3-a0bc-c345c36f2c84">CreateWellKnownSid</a> function to create a SID from this list.


## -enum-fields




### -field WinNullSid

Indicates a null SID.


### -field WinWorldSid

Indicates a SID that matches everyone.


### -field WinLocalSid

Indicates a local SID.


### -field WinCreatorOwnerSid

Indicates a SID that matches the owner or creator of an object.


### -field WinCreatorGroupSid

Indicates a SID that matches the creator group of an object.


### -field WinCreatorOwnerServerSid

Indicates a creator owner server SID.


### -field WinCreatorGroupServerSid

Indicates a creator group server SID.


### -field WinNtAuthoritySid

Indicates a SID for the Windows NT authority account.


### -field WinDialupSid

Indicates a SID for a dial-up account.


### -field WinNetworkSid

Indicates a SID for a network account. This SID is added to the process of a token when it logs on across a network. The corresponding logon type is LOGON32_LOGON_NETWORK.


### -field WinBatchSid

Indicates a SID for a batch process. This SID is added to the process of a token when it logs on as a batch job. The corresponding logon type is LOGON32_LOGON_BATCH.


### -field WinInteractiveSid

Indicates a SID for an interactive account. This SID is added to the process of a token when it logs on interactively. The corresponding logon type is LOGON32_LOGON_INTERACTIVE.


### -field WinServiceSid

Indicates a SID for a service. This SID is added to the process of a token when it logs on as a service. The corresponding logon type is LOGON32_LOGON_SERVICE.


### -field WinAnonymousSid

Indicates a SID for the anonymous account.


### -field WinProxySid

Indicates a proxy SID.


### -field WinEnterpriseControllersSid

Indicates a SID for an enterprise controller.


### -field WinSelfSid

Indicates a SID for self.


### -field WinAuthenticatedUserSid

Indicates a SID that matches any authenticated user.


### -field WinRestrictedCodeSid

Indicates a SID for restricted code.


### -field WinTerminalServerSid

Indicates a SID that matches a terminal server account.


### -field WinRemoteLogonIdSid

Indicates a SID that matches remote logons.


### -field WinLogonIdsSid

Indicates a SID that matches logon IDs.


### -field WinLocalSystemSid

Indicates a SID that matches the local system.


### -field WinLocalServiceSid

Indicates a SID that matches a local service.


### -field WinNetworkServiceSid

Indicates a SID that matches a network service.


### -field WinBuiltinDomainSid

Indicates a SID that matches the domain account.


### -field WinBuiltinAdministratorsSid

Indicates a SID that matches the administrator group.


### -field WinBuiltinUsersSid

Indicates a SID that matches built-in user accounts.


### -field WinBuiltinGuestsSid

Indicates a SID that matches the guest account.


### -field WinBuiltinPowerUsersSid

Indicates a SID that matches the power users group.


### -field WinBuiltinAccountOperatorsSid

Indicates a SID that matches the account operators account.


### -field WinBuiltinSystemOperatorsSid

Indicates a SID that matches the system operators group.


### -field WinBuiltinPrintOperatorsSid

Indicates a SID that matches the print operators group.


### -field WinBuiltinBackupOperatorsSid

Indicates a SID that matches the backup operators group.


### -field WinBuiltinReplicatorSid

Indicates a SID that matches the replicator account.


### -field WinBuiltinPreWindows2000CompatibleAccessSid

Indicates a SID that matches pre-Windows 2000 compatible accounts.


### -field WinBuiltinRemoteDesktopUsersSid

Indicates a SID that matches remote desktop users.


### -field WinBuiltinNetworkConfigurationOperatorsSid

Indicates a SID that matches the network operators group.


### -field WinAccountAdministratorSid

Indicates a SID that matches the account administrator's account.


### -field WinAccountGuestSid

Indicates a SID that matches the account guest group.


### -field WinAccountKrbtgtSid

Indicates a SID that matches account Kerberos target group.


### -field WinAccountDomainAdminsSid

Indicates a SID that matches the account domain administrator group.


### -field WinAccountDomainUsersSid

Indicates a SID that matches the account domain users group.


### -field WinAccountDomainGuestsSid

Indicates a SID that matches the account domain guests group.


### -field WinAccountComputersSid

Indicates a SID that matches the account computer group.


### -field WinAccountControllersSid

Indicates a SID that matches the account controller group.


### -field WinAccountCertAdminsSid

Indicates a SID that matches the certificate administrators group.


### -field WinAccountSchemaAdminsSid

Indicates a SID that matches the schema administrators group.


### -field WinAccountEnterpriseAdminsSid

Indicates a SID that matches the enterprise administrators group.


### -field WinAccountPolicyAdminsSid

Indicates a SID that matches the policy administrators group.


### -field WinAccountRasAndIasServersSid

Indicates a SID that matches the RAS and IAS server account.


### -field WinNTLMAuthenticationSid

Indicates a SID present when the Microsoft NTLM authentication package authenticated the client.


### -field WinDigestAuthenticationSid

Indicates a SID present when the Microsoft Digest authentication package authenticated the client.


### -field WinSChannelAuthenticationSid

Indicates a SID present when the Secure Channel (SSL/TLS) authentication package authenticated the client.


### -field WinThisOrganizationSid

Indicates a SID present when the user authenticated from within the forest or across a trust that does not have the selective authentication option enabled. If this SID is present, then WinOtherOrganizationSid cannot be present.


### -field WinOtherOrganizationSid

Indicates a SID present when the user authenticated across a forest with the selective authentication option enabled. If this SID is present, then WinThisOrganizationSid cannot be present.


### -field WinBuiltinIncomingForestTrustBuildersSid

Indicates a SID that allows a user to create incoming forest trusts. It is added to the token of users who are a member of the Incoming Forest Trust Builders built-in group in the root domain of the forest.


### -field WinBuiltinPerfMonitoringUsersSid

Indicates a SID that matches the performance monitor user group.


### -field WinBuiltinPerfLoggingUsersSid

Indicates a SID that matches the performance log user group.


### -field WinBuiltinAuthorizationAccessSid

Indicates a SID that matches the Windows Authorization Access group.


### -field WinBuiltinTerminalServerLicenseServersSid

Indicates a SID is present in a server that can issue terminal server licenses.


### -field WinBuiltinDCOMUsersSid

Indicates a SID that matches the distributed COM user group.


### -field WinBuiltinIUsersSid

Indicates a SID that matches the Internet  built-in user group.


### -field WinIUserSid

Indicates a SID that matches the Internet user group.


### -field WinBuiltinCryptoOperatorsSid

Indicates a SID that allows a user to use cryptographic operations. It is added to the token of users who are a member of the CryptoOperators built-in group. 


### -field WinUntrustedLabelSid

Indicates a SID that matches an untrusted label.


### -field WinLowLabelSid

Indicates a SID that matches an low level of trust label.


### -field WinMediumLabelSid

Indicates a SID that matches an medium level of trust label.


### -field WinHighLabelSid

Indicates a SID that matches a high level of trust label.


### -field WinSystemLabelSid

Indicates a SID that matches a system label.


### -field WinWriteRestrictedCodeSid

Indicates a SID that matches a write restricted code group.


### -field WinCreatorOwnerRightsSid

Indicates a SID that matches a creator and owner rights group.


### -field WinCacheablePrincipalsGroupSid

Indicates a SID that matches a cacheable principals group.


### -field WinNonCacheablePrincipalsGroupSid

Indicates a SID that matches a non-cacheable principals group.


### -field WinEnterpriseReadonlyControllersSid

Indicates a SID that matches an enterprise wide read-only controllers group.


### -field WinAccountReadonlyControllersSid

Indicates a SID that matches an account read-only controllers group.


### -field WinBuiltinEventLogReadersGroup

Indicates a SID that matches an event log readers group.


### -field WinNewEnterpriseReadonlyControllersSid

Indicates a SID that matches a read-only enterprise domain controller.


### -field WinBuiltinCertSvcDComAccessGroup

Indicates a SID that matches the built-in DCOM certification services access group.


### -field WinMediumPlusLabelSid

Indicates a SID that matches the medium plus integrity label.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinLocalLogonSid

Indicates a SID that matches a local logon group.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinConsoleLogonSid

Indicates a SID that matches a console logon group.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinThisOrganizationCertificateSid

Indicates a SID that matches a certificate for the given organization.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinApplicationPackageAuthoritySid

Indicates a SID that matches the application package authority.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinBuiltinAnyPackageSid

Indicates a SID that applies to all app containers.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinCapabilityInternetClientSid

Indicates a SID of Internet client capability for app containers.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinCapabilityInternetClientServerSid

Indicates a SID of Internet client and server capability for app containers.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinCapabilityPrivateNetworkClientServerSid

Indicates a SID of private network client and server capability for app containers.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinCapabilityPicturesLibrarySid

Indicates a SID for pictures library capability for app containers.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinCapabilityVideosLibrarySid

Indicates a SID for videos library capability for app containers.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinCapabilityMusicLibrarySid

Indicates a SID for music library capability for app containers.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinCapabilityDocumentsLibrarySid

Indicates a SID for documents library capability for app containers.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinCapabilitySharedUserCertificatesSid

Indicates a SID for shared user certificates capability for app containers.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinCapabilityEnterpriseAuthenticationSid

Indicates a SID for Windows credentials capability for app containers.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinCapabilityRemovableStorageSid

Indicates a SID for removable storage capability for app containers.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not available.


### -field WinBuiltinRDSRemoteAccessServersSid


### -field WinBuiltinRDSEndpointServersSid


### -field WinBuiltinRDSManagementServersSid


### -field WinUserModeDriversSid


### -field WinBuiltinHyperVAdminsSid


### -field WinAccountCloneableControllersSid


### -field WinBuiltinAccessControlAssistanceOperatorsSid


### -field WinBuiltinRemoteManagementUsersSid


### -field WinAuthenticationAuthorityAssertedSid


### -field WinAuthenticationServiceAssertedSid


### -field WinLocalAccountSid


### -field WinLocalAccountAndAdministratorSid


### -field WinAccountProtectedUsersSid


### -field WinCapabilityAppointmentsSid


### -field WinCapabilityContactsSid


### -field WinAccountDefaultSystemManagedSid


### -field WinBuiltinDefaultSystemManagedGroupSid


### -field WinBuiltinStorageReplicaAdminsSid


### -field WinAccountKeyAdminsSid


### -field WinAccountEnterpriseKeyAdminsSid


### -field WinAuthenticationKeyTrustSid


### -field WinAuthenticationKeyPropertyMFASid


### -field WinAuthenticationKeyPropertyAttestationSid


### -field WinAuthenticationFreshKeyAuthSid


### -field WinBuiltinDeviceOwnersSid




## -see-also




<a href="https://msdn.microsoft.com/3d813e46-f06e-4147-874c-30b5fc6f50d9">Allowing Anonymous Access</a>



<a href="https://msdn.microsoft.com/00e75bae-fbce-41a3-a0bc-c345c36f2c84">CreateWellKnownSid</a>



<a href="https://msdn.microsoft.com/1a08c70c-00fa-4c62-883d-4f17f9d7c04b">IsWellKnownSid</a>



<a href="https://msdn.microsoft.com/eb2f95c4-9465-409b-b76c-9ccae1d05eda">Well-known SIDs</a>
 

 


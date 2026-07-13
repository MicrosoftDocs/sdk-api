---
UID: NF:ntdsapi.DsAddSidHistoryW
title: DsAddSidHistoryW function (ntdsapi.h)
description: Retrieves the primary account security identifier (SID) of a security principal from one domain and adds it to the sIDHistory attribute of a security principal in another domain in a different forest. (Unicode)
helpviewer_keywords: ["DsAddSidHistory", "DsAddSidHistory function [Active Directory]", "DsAddSidHistoryW", "_glines_dsaddsidhistory", "ad.dsaddsidhistory", "ntdsapi/DsAddSidHistory", "ntdsapi/DsAddSidHistoryW"]
old-location: ad\dsaddsidhistory.htm
tech.root: ad
ms.assetid: 36ef8734-717a-4c3a-a839-6591d85c9734
ms.date: 12/05/2018
ms.keywords: DsAddSidHistory, DsAddSidHistory function [Active Directory], DsAddSidHistoryA, DsAddSidHistoryW, _glines_dsaddsidhistory, ad.dsaddsidhistory, ntdsapi/DsAddSidHistory, ntdsapi/DsAddSidHistoryA, ntdsapi/DsAddSidHistoryW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsAddSidHistoryW (Unicode) and DsAddSidHistoryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsAddSidHistoryW
 - ntdsapi/DsAddSidHistoryW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsAddSidHistory
 - DsAddSidHistoryA
 - DsAddSidHistoryW
---

# DsAddSidHistoryW function


## -description

The <b>DsAddSidHistory</b> function retrieves the primary account security identifier (SID) of a security principal from one domain and adds it to the <b>sIDHistory</b> attribute of a security principal in another domain in a different forest. When the source domain is in Windows 2000 native mode, this function also retrieves the <b>sIDHistory</b> values of the source principal and adds them to the destination principal <b>sIDHistory</b>.

The <b>DsAddSidHistory</b> function performs a security-sensitive function by adding the primary account SID of an existing security principal to the <b>sIDHistory</b> of a principal in a domain in a different forest, effectively granting to the latter access to all resources accessible to the former. For  more information about the use and security implications of this function, see <a href="/windows/desktop/AD/using-dsaddsidhistory">Using DsAddSidHistory</a>.

## -parameters

### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param Flags [in]

Reserved for future use. Set to <b>NULL</b>.

### -param SrcDomain [in]

Pointer to a null-terminated string that specifies the name of the domain to query for the SID of <i>SrcPrincipal</i>.

If the source domain runs on  Windows Server operating systems, <i>SrcDomain</i> can be either a domain name system (DNS) name, for example, fabrikam.com, or a flat NetBIOS, for example, Fabrikam, name. DNS names should be used when possible.

### -param SrcPrincipal [in]

Pointer to a null-terminated string that specifies the name of a security principal, user or group, in the source domain. This name is a domain-relative Security Account Manager (SAM) name, for example: evacorets.

### -param SrcDomainController [in]

Pointer to a null-terminated string that specifies the name of the primary domain controller (PDC) Emulator in the source domain to use for secure retrieval of the source principal SID and audit generation. 


If this parameter is <b>NULL</b>, <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> will select the primary domain controller.

<i>SrcDomainController</i> can be either a DNS name or a flat NetBIOS name. DNS names should be used when possible.

### -param SrcDomainCreds [in]

Contains an identity handle that represents the identity and credentials of a user with administrative rights in the source domain. To obtain this handle, call  <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa">DsMakePasswordCredentials</a>. This user must be a member of either the Administrators or the Domain Administrators group. If this call is made from a remote computer to the destination DC, then both the remote computer and the destination DC must support 128-bit encryption to privacy-protect the credentials. If 128-bit encryption is unavailable and <i>SrcDomainCreds</i> are provided, then the call must be made on the destination DC.

If this parameter is <b>NULL</b>, the credentials of the caller are used for access to the source domain.

### -param DstDomain [in]

Pointer to a null-terminated string that specifies the name of the destination domain in which <i>DstPrincipal</i> resides. This name can either be a DNS name, for example, fabrikam.com, or a NetBIOS name, for example, Fabrikam. The destination domain must run Windows 2000 native mode.

### -param DstPrincipal [in]

Pointer to a null-terminated string that specifies the name of a security principal, user or group, in the destination domain. This domain-relative SAM name identifies the principal whose <b>sIDHistory</b> attribute is updated with the SID of the <i>SrcPrincipal</i>.

## -returns

Returns a Win32 error codes including the following.

## -see-also

<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa">DsMakePasswordCredentials</a>



<a href="/windows/desktop/AD/using-dsaddsidhistory">Using DsAddSidHistory</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind_s">ldap_bind_s</a>



<b>ldap_open</b>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DsAddSidHistory as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

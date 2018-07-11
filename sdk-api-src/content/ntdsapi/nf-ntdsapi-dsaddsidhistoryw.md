---
UID: NF:ntdsapi.DsAddSidHistoryW
title: DsAddSidHistoryW function
author: windows-sdk-content
description: Retrieves the primary account security identifier (SID) of a security principal from one domain and adds it to the sIDHistory attribute of a security principal in another domain in a different forest.
old-location: ad\dsaddsidhistory.htm
old-project: ad
ms.assetid: 36ef8734-717a-4c3a-a839-6591d85c9734
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: DsAddSidHistory, DsAddSidHistory function [Active Directory], DsAddSidHistoryA, DsAddSidHistoryW, _glines_dsaddsidhistory, ad.dsaddsidhistory, ntdsapi/DsAddSidHistory, ntdsapi/DsAddSidHistoryA, ntdsapi/DsAddSidHistoryW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: DS_REPL_OP_TYPE
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
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# DsAddSidHistoryW function


## -description


The <b>DsAddSidHistory</b> function retrieves the primary account security identifier (SID) of a security principal from one domain and adds it to the <b>sIDHistory</b> attribute of a security principal in another domain in a different forest. When the source domain is in Windows 2000 native mode, this function also retrieves the <b>sIDHistory</b> values of the source principal and adds them to the destination principal <b>sIDHistory</b>.

The <b>DsAddSidHistory</b> function performs a security-sensitive function by adding the primary account SID of an existing security principal to the <b>sIDHistory</b> of a principal in a domain in a different forest, effectively granting to the latter access to all resources accessible to the former. For  more information about the use and security implications of this function, see <a href="https://msdn.microsoft.com/cbf4983c-551d-4771-870e-a192ed898eb7">Using DsAddSidHistory</a>.


## -parameters




### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param Flags [in]

Reserved for future use. Set to <b>NULL</b>.


### -param SrcDomain [in]

Pointer to a null-terminated string that specifies the name of the domain to query for the SID of <i>SrcPrincipal</i>.

If the source domain runs on  Windows Server operating systems, <i>SrcDomain</i> can be either a domain name system (DNS) name, for example, fabrikam.com, or a flat NetBIOS, for example, Fabrikam, name. DNS names should be used when possible.


### -param SrcPrincipal [in]

Pointer to a null-terminated string that specifies the name of a security principal, user or group, in the source domain. This name is a domain-relative Security Account Manager (SAM) name, for example: evacorets.


### -param SrcDomainController [in]

Pointer to a null-terminated string that specifies the name of the primary domain controller (PDC) Emulator in the source domain to use for secure retrieval of the source principal SID and audit generation. 


If this parameter is <b>NULL</b>, <a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> will select the primary domain controller.

<i>SrcDomainController</i> can be either a DNS name or a flat NetBIOS name. DNS names should be used when possible.


### -param SrcDomainCreds [in]

Contains an identity handle that represents the identity and credentials of a user with administrative rights in the source domain. To obtain this handle, call  <a href="https://msdn.microsoft.com/51aba58b-07c5-4e6d-8568-fa6f1a963d8e">DsMakePasswordCredentials</a>. This user must be a member of either the Administrators or the Domain Administrators group. If this call is made from a remote computer to the destination DC, then both the remote computer and the destination DC must support 128-bit encryption to privacy-protect the credentials. If 128-bit encryption is unavailable and <i>SrcDomainCreds</i> are provided, then the call must be made on the destination DC.

If this parameter is <b>NULL</b>, the credentials of the caller are used for access to the source domain.


### -param DstDomain [in]

Pointer to a null-terminated string that specifies the name of the destination domain in which <i>DstPrincipal</i> resides. This name can either be a DNS name, for example, fabrikam.com, or a NetBIOS name, for example, Fabrikam. The destination domain must run Windows 2000 native mode.


### -param DstPrincipal [in]

Pointer to a null-terminated string that specifies the name of a security principal, user or group, in the destination domain. This domain-relative SAM name identifies the principal whose <b>sIDHistory</b> attribute is updated with the SID of the <i>SrcPrincipal</i>.


## -returns



Returns a Win32 error codes including the following.




## -see-also




<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/51aba58b-07c5-4e6d-8568-fa6f1a963d8e">DsMakePasswordCredentials</a>



<a href="https://msdn.microsoft.com/cbf4983c-551d-4771-870e-a192ed898eb7">Using DsAddSidHistory</a>



<a href="https://msdn.microsoft.com/67d30a7b-2f42-4e1a-8c59-5ba22ed3fad4">ldap_bind_s</a>



<b>ldap_open</b>
 

 


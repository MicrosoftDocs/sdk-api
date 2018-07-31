---
UID: NF:wincred.CredReadDomainCredentialsA
title: CredReadDomainCredentialsA function
author: windows-sdk-content
description: Reads the domain credentials from the user's credential set.
old-location: security\credreaddomaincredentials.htm
old-project: SecAuthN
ms.assetid: b62cb9c9-2a64-4ef4-97f0-e1ea85976d3e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CredReadDomainCredentials, CredReadDomainCredentials function [Security], CredReadDomainCredentialsA, CredReadDomainCredentialsW, _cred_credreaddomaincredentials, security.credreaddomaincredentials, wincred/CredReadDomainCredentials, wincred/CredReadDomainCredentialsA, wincred/CredReadDomainCredentialsW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredReadDomainCredentialsW (Unicode) and CredReadDomainCredentialsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CRED_PROTECTION_TYPE, *PCRED_PROTECTION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-0.dll
 - sechost.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
 - CredReadDomainCredentials
 - CredReadDomainCredentialsA
 - CredReadDomainCredentialsW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CredReadDomainCredentialsA function


## -description


The <b>CredReadDomainCredentials</b> function reads the domain credentials from the user's credential set. The credential set used is the one associated with the logon session of the current token. The token must not have the user's SID disabled.


## -parameters




### -param TargetInfo [in]

Target information that identifies the target server. At least one of the naming members must not be <b>NULL</b>: NetbiosServerName, DnsServerName, NetbiosDomainName, DnsDomainName or DnsTreeName.


### -param Flags [in]

Flags controlling the operation of the function. 




The following flag is defined:

CRED_CACHE_TARGET_INFORMATION

Cache the TargetInfo for a subsequent read using <a href="https://msdn.microsoft.com/14dca0af-72d7-4ca8-84bb-c7040c5b5fb9">CredGetTargetInfo</a>.


### -param Count [out]

Count of the credentials returned in the <i>Credentials</i> array.


### -param Credential

TBD




#### - Credentials [out]

Pointer to an array of pointers to credentials. The most specific existing credential matching the <i>TargetInfo</i> is returned. If credentials of various types (for example, CRED_TYPE_DOMAIN_PASSWORD and CRED_TYPE_DOMAIN_CERTIFICATE credentials) exist, one of each type is returned. If a connection were to be made to the named target, this most-specific credential would be used. 




Only those credential types specified by the <i>TargetInfo</i>.CredTypes array are returned. The returned <i>Credentials</i> array is sorted in the same order as the <i>TargetInfo</i>.CredTypes array. That is, authentication packages specify a preferred credential type by specifying it earlier in the <i>TargetInfo</i>.CredTypes array.If <i>TargetInfo</i>.CredTypeCount is zero, the <i>Credentials</i> array is returned in the following sorted order:

<ul>
<li>CRED_TYPE_DOMAIN_CERTIFICATE</li>
<li>CRED_TYPE_DOMAIN_PASSWORD</li>
</ul>


The returned buffer is a single allocated block. Any pointers contained within the buffer are pointers to locations within this single allocated block. The single returned buffer must be freed by calling <a href="https://msdn.microsoft.com/bc33ab1b-dd3f-4e1b-96d2-e32ceff89ada">CredFree</a>.


## -returns



The function returns <b>TRUE</b> on success and <b>FALSE</b> on failure. The <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function can be called to get a more specific status code. The following status codes can be returned:

<ul>
<li>ERROR_INVALID_PARAMETER 


None of the naming parameters were specified.

</li>
<li>ERROR_NOT_FOUND 


There are no credentials matching the specified naming parameters.

</li>
<li>ERROR_NO_SUCH_LOGON_SESSION 


The logon session does not exist or there is no credential set associated with this logon session. Network logon sessions do not have an associated credential set.

</li>
<li>ERROR_INVALID_FLAGS 


A flag that is not valid was specified for the <i>Flags</i> parameter.

</li>
</ul>



## -remarks



This function returns the most specific credentials matching the naming parameters. For instance, if there is a credential that matches the target server name and a credential that matches the target domain name, only the server specific credential is returned. This is the credential that would be used.

The following list specifies the order (from most specific to least specific) of what credential is returned if more than one matches:

<ul>
<li>The credential target name is of the form &lt;<i>DfsRoot</i>&gt;\&lt;<i>DfsShare</i>&gt;, and it is an exact match on the <i>TargetName</i>.</li>
<li>An exact match on the <i>DnsServerName</i>.</li>
<li>An exact match on the <i>NetBIOSServerName</i>.</li>
<li>An exact match on <i>TargetName</i>.</li>
<li>A match of the <i>DnsServerName</i> to a wildcard server credential. If more than one wildcard server credential matches, the credential with the longer TargetName is used. That is, a credential for *.example.microsoft.com is used instead of a credential for *.microsoft.com.</li>
<li>An exact match of the <i>DnsDomainName</i> to a wildcard domain credential of the form &lt;<i>DnsDomainName</i>&gt;\*.</li>
<li>An exact match of the <i>NetBIOSDomainName </i>to a wildcard domain credential of the form &lt;<i>NetBIOSDomainName</i>&gt;\*</li>
<li>The credential named CRED_SESSION_WILDCARD_NAME.</li>
<li>The credential named "*".</li>
</ul>
<b>CredReadDomainCredentials</b> differs from <a href="https://msdn.microsoft.com/3222de7b-5290-4e82-a382-b2db6afc78cc">CredRead</a> in that it handles the idiosyncrasies of domain (CRED_TYPE_DOMAIN_PASSWORD or CRED_TYPE_DOMAIN_CERTIFICATE) credentials. Domain credentials contain more than one target member.

If the value of the <b>Type</b> member of the <a href="https://msdn.microsoft.com/6361b93c-4441-4a01-bd39-b95c42962497">CREDENTIAL</a> structure specified by the <i>Credentials</i>  parameter is <b>CRED_TYPE_DOMAIN_EXTENDED</b>, a namespace must be specified in the target name. This function can return only one credential of the specified type.

This function can return multiple credentials of this type, but <b>CRED_TYPE_DOMAIN_EXTENDED</b> cannot be mixed with other types in the <b>CredTypes</b> member of the <a href="https://msdn.microsoft.com/92180f2c-ef7c-4481-9b6f-19234c114afb">CREDENTIAL_TARGET_INFORMATION</a> structure specified by the <i>TargetInfo</i> parameter.




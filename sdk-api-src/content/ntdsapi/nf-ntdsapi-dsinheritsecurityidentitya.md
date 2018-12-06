---
UID: NF:ntdsapi.DsInheritSecurityIdentityA
title: DsInheritSecurityIdentityA function
author: windows-sdk-content
description: Appends the objectSid and sidHistory attributes of SrcPrincipal to the sidHistory of DstPrincipal and then deletes SrcPrincipal, all in a single transaction.
old-location: ad\dsinheritsecurityidentity.htm
tech.root: ad
ms.assetid: ea467069-f886-4e22-896c-16e6e01f3968
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DsInheritSecurityIdentity, DsInheritSecurityIdentity function [Active Directory], DsInheritSecurityIdentityA, DsInheritSecurityIdentityW, _glines_dsinheritsecurityidentity, ad.dsinheritsecurityidentity, ntdsapi/DsInheritSecurityIdentity, ntdsapi/DsInheritSecurityIdentityA, ntdsapi/DsInheritSecurityIdentityW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsInheritSecurityIdentityW (Unicode) and DsInheritSecurityIdentityA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsInheritSecurityIdentity
 - DsInheritSecurityIdentityA
 - DsInheritSecurityIdentityW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsInheritSecurityIdentityA function


## -description


The <b>DsInheritSecurityIdentity</b> function appends the <b>objectSid</b> and <b>sidHistory</b> attributes of <i>SrcPrincipal</i> to the <b>sidHistory</b> of <i>DstPrincipal</i> and then deletes <i>SrcPrincipal</i>, all in a single transaction. To ensure that this operation is atomic, <i>SrcPrincipal</i> and <i>DstPrincipal</i> must be in the same domain and <i>hDS</i> must be bound to  a domain controller that the correct permissions within that domain.


## -parameters




### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param Flags [in]

Reserved for future use. Must be zero.


### -param SrcPrincipal [in]

Pointer to a null-terminated string that specifies the name of a security principal (user or group) in the source domain. This name is a domain-relative SAM name.


### -param DstPrincipal [in]

Pointer to a null-terminated string that specifies the name of a security principal (user or group) in the destination domain. This domain-relative SAM name identifies the principal whose <b>sidHistory</b> attribute will be updated with the SID of <i>SrcPrincipal</i>.


## -returns



Returns a system or RPC error code including the following.




## -remarks



With an operating system upgrade domain applications, which span both upgraded and non-upgraded domains, may have security principals inside and outside the forest for the same logical entity at the same time.

When all upgraded domains have joined the same forest, <b>DsInheritSecurityIdentity</b> eliminates the duplicate objects while ensuring that the remaining objects have all the security rights and privileges belonging to their respective deleted object.

A <b>DsInheritSecurityIdentity</b> implementation:

<ul>
<li>Verifies that <i>SrcPrincipal</i> and <i>DstPrincipal</i> are in the same domain.</li>
<li>Verifies that the domain is writable at the bind to the server.</li>
<li>Verifies that auditing is enabled for the domain.</li>
<li>Verifies that the caller is a member of the domain administrators for the domain.</li>
<li>Verifies that the domain is in the native mode.</li>
<li>Verifies that <i>SrcPrincipal</i> exists, that it is a security principal and has read its <b>objectSid</b> and <b>sidHistory</b> properties.</li>
<li>Verifies that <i>DstPrincipal</i> exists, that it is a security principal, and has read certain properties required for auditing and verification.</li>
<li>Deletes <i>SrcPrincipal</i> in the database only if the entire operation is committed at completion. This operation fails if the caller does not have delete rights or if <i>SrcPrincipal</i> has children.</li>
<li>Fails the operation if the <b>objectSid</b> of <i>SrcPrincipal</i> or <i>DstPrincipal</i> is a well-known SID.</li>
<li>Adds the <b>objectSid</b> and the <b>sidHistory</b> (if present) of <i>SrcPrincipal</i> to the <b>sidHistory</b> of <i>DstPrincipal</i>.</li>
<li>Forces an audit event and fails the operation if the audit fails.</li>
<li>Enters events into the Directory Service Log. Do not confuse this with the Security Audit Log.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>
 

 


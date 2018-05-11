---
UID: NF:ntsecapi.LsaQueryForestTrustInformation
title: LsaQueryForestTrustInformation function
author: windows-driver-content
description: Retrieves forest trust information for the specified Local Security Authority&#160;TrustedDomain object.
old-location: security\lsaqueryforesttrustinformation.htm
old-project: SecAuthN
ms.assetid: 38857f1f-e2c7-4ce5-a928-335bc3bd2176
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: LsaQueryForestTrustInformation, LsaQueryForestTrustInformation function [Security], ntsecapi/LsaQueryForestTrustInformation, security.lsaqueryforesttrustinformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
api_name:
-	LsaQueryForestTrustInformation
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LsaQueryForestTrustInformation function


## -description


The <b>LsaQueryForestTrustInformation</b> function retrieves forest trust information
    for the specified <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> object.


## -parameters




### -param PolicyHandle [in]

A handle to the <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object for the system.


### -param TrustedDomainName [in]

Pointer to an <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that contains the name of the <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> object for which to retrieve forest trust information.


### -param ForestTrustInfo [out]

Pointer to an <a href="https://msdn.microsoft.com/9e456462-59a9-4f18-ba47-92fc2350889b">LSA_FOREST_TRUST_INFORMATION</a> structure that returns the forest trust information for the <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> object specified by the <i>TrustedDomainName</i> parameter.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be one of the following values or one of the <a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_DOMAIN_ROLE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The operation is legal only on the primary
                                    domain controller.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_DOMAIN_STATE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The operation is legal only on domain
                                    controllers in the root domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_DOMAIN</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The specified <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> object does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_FOUND</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The specified <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> object does not contain forest trust information.

</td>
</tr>
</table>
 




## -remarks



Access to this function is protected by a securable object.




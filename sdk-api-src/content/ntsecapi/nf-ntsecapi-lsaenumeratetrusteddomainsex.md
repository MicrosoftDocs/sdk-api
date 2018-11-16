---
UID: NF:ntsecapi.LsaEnumerateTrustedDomainsEx
title: LsaEnumerateTrustedDomainsEx function
author: windows-sdk-content
description: Returns information about the domains trusted by the local system.
old-location: security\lsaenumeratetrusteddomainsex.htm
tech.root: SecMgmt
ms.assetid: 4a203bff-c3e1-4d95-b556-617dc8c2e8c2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: LsaEnumerateTrustedDomainsEx, LsaEnumerateTrustedDomainsEx function [Security], _lsa_lsaenumeratetrusteddomainsex, ntsecapi/LsaEnumerateTrustedDomainsEx, security.lsaenumeratetrusteddomainsex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntsecapi.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - LsaEnumerateTrustedDomainsEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- LsaEnumerateTrustedDomainsEx
: 
---

# LsaEnumerateTrustedDomainsEx function


## -description


The <b>LsaEnumerateTrustedDomainsEx</b> function returns information about the domains trusted by the local system.<b>LsaEnumerateTrustedDomainsEx</b> returns information only on direct trusts. 
<a href="https://msdn.microsoft.com/6c3b788f-ee53-4637-acdb-04316e8464fe">DsEnumerateDomainTrusts</a> is recommended for more complete trust enumeration purposes.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. This call requires POLICY_VIEW_LOCAL_INFORMATION access to the <b>Policy</b> object. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param EnumerationContext [in]

A pointer to an 
<a href="https://msdn.microsoft.com/99dad3aa-cb92-4b7e-8a18-2c977cb2737c">LSA_ENUMERATION_HANDLE</a> that you can use to make multiple calls to <b>LsaEnumerateTrustedDomainsEx</b>  to retrieve all of the trusted domain information. For more information, see Remarks.


### -param Buffer [out]

Pointer to a buffer that receives a list of 
<a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a> structures that contain information about the enumerated trusted domains. 




Your application should free this buffer when it is no longer needed by calling 
<a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a>.


### -param PreferedMaximumLength [in]

Preferred maximum length, in bytes, of returned data. This is not a hard upper limit, but serves as a guide. Due to data conversion between systems with different natural data sizes, the actual amount of data returned may be greater than this value.


### -param CountReturned [out]

Pointer to a <b>LONG</b> that receives the number of trusted domain objects returned.


## -returns



If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an  <b>NTSTATUS</b> code, which can be one of the following values or one of the 
<a href="management_return_values.htm">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Caller does not have the appropriate access to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MORE_ENTRIES</b></dt>
</dl>
</td>
<td width="60%">
There are no more entries. This warning is returned if no objects have been enumerated because the <i>EnumerationContext</i> value is too high.

</td>
</tr>
</table>
 

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> code to a Windows error code.




## -remarks



Retrieving all trust information may require more than a single <b>LsaEnumerateTrustedDomainsEx</b> call.

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To use the <i>EnumerationContext</i> parameter to make multiple calls</b>

<ol>
<li>Set the variable pointed to by <i>EnumerationContext</i> to zero.</li>
<li>If <b>LsaEnumerateTrustedDomainsEx</b> returns STATUS_SUCCESS or STATUS_MORE_ENTRIES, call the function again, passing in the <i>EnumerationContext</i> value returned by the previous call.</li>
<li>The enumeration is complete when the function returns STATUS_NO_MORE_ENTRIES.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/99dad3aa-cb92-4b7e-8a18-2c977cb2737c">LSA_ENUMERATION_HANDLE</a>



<a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a>



<a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a>
 

 


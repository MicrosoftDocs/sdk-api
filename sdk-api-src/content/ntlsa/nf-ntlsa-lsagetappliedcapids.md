---
UID: NF:ntlsa.LsaGetAppliedCAPIDs
title: LsaGetAppliedCAPIDs function (ntlsa.h)
description: Returns an array of central access policies (CAPs) identifiers (CAPIDs) of all the CAPs applied on a specific computer.
helpviewer_keywords: ["LsaGetAppliedCAPIDs","LsaGetAppliedCAPIDs function [Security]","ntlsa/LsaGetAppliedCAPIDs","security.lsagetappliedcapids"]
old-location: security\lsagetappliedcapids.htm
tech.root: security
ms.assetid: DF10F5CE-BBF5-4CA8-919B-F59B7775C983
ms.date: 12/05/2018
ms.keywords: LsaGetAppliedCAPIDs, LsaGetAppliedCAPIDs function [Security], ntlsa/LsaGetAppliedCAPIDs, security.lsagetappliedcapids
req.header: ntlsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LsaGetAppliedCAPIDs
 - ntlsa/LsaGetAppliedCAPIDs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - LsaGetAppliedCAPIDs
---

# LsaGetAppliedCAPIDs function


## -description

The <b>LsaGetAppliedCAPIDs</b> function returns an array of central access policies (CAPs) identifiers (CAPIDs) of all the CAPs applied on a specific computer.

## -parameters

### -param SystemName [in, optional]

A pointer to an <a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that contains the name of the specific computer. The name can have the form of "ComputerName" or "\\ComputerName". If this parameter is <b>NULL</b>, then the function returns the CAPIDs of the local computer.

### -param CAPIDs [out]

A pointer to a variable that receives an array of pointers to CAPIDs that identify the CAPs available on the specified computer. When you have finished using the CAPIDs, call the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsafreememory">LsaFreeMemory</a> function on each element in the array and the entire array.

### -param CAPIDCount [out]

A pointer to a variable that receives the number of CAPs that are available on the specified computer. The array returned in the <i>CAPIDs</i> parameter contains the same number of elements as the <i>CAPIDCount</i> parameter.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is one of the <a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>. You can use the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to  convert the <b>NTSTATUS</b> code to a Windows error code.

## -remarks

For specific details about the central access policies, you can query the attributes of the central access policy object in the Active Directory on the specified computer's domain controller.  Look for the object whose <b>msAuthz-CentralAccessPolicyID</b> attribute matches one of the returned CAPIDs.

## -see-also

<a href="/windows/desktop/SecAuthZ/centralized-authorization-policy">Centralized Authorization Policy</a>
---
UID: NF:msdrm.DRMGetUnboundLicenseAttributeCount
title: DRMGetUnboundLicenseAttributeCount function (msdrm.h)
description: Retrieves the number of occurrences of an attribute within an object in an unbound license.
helpviewer_keywords: ["DRMGetUnboundLicenseAttributeCount","DRMGetUnboundLicenseAttributeCount function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetUnboundLicenseAttributeCount","rm.drmgetunboundlicenseattributecount"]
old-location: rm\drmgetunboundlicenseattributecount.htm
tech.root: rm
ms.assetid: ea462757-9df8-4b50-966b-5998e570f321
ms.date: 12/05/2018
ms.keywords: DRMGetUnboundLicenseAttributeCount, DRMGetUnboundLicenseAttributeCount function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetUnboundLicenseAttributeCount, rm.drmgetunboundlicenseattributecount
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
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
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - DRMGetUnboundLicenseAttributeCount
 - msdrm/DRMGetUnboundLicenseAttributeCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMGetUnboundLicenseAttributeCount
---

# DRMGetUnboundLicenseAttributeCount function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetUnboundLicenseAttributeCount</b> function retrieves the number of occurrences of an attribute within an object in an unbound license.

## -parameters

### -param hQueryRoot [in]

A handle to a license or an object in the license, created using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseobject">DRMGetUnboundLicenseObject</a> or <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmparseunboundlicense">DRMParseUnboundLicense</a>.

### -param wszAttributeType [in]

Name of the attribute to retrieve.

### -param pcAttributes [out]

Count of attribute occurrences one level down within the specified branch.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Certain attributes, such as maximum count, may appear more than once in a branch of a license. This method returns a count of these occurrences, so that an application can iterate through them or access a particular one. This query will search only at the level immediately below the passed in object. So, for example, if the root license handle is passed in and the attribute to find is g_wszQUERY_SKUVALUE, the query will find nothing because the SKUVALUE appears at the second level or deeper (counting the license root as level 0).

## -see-also

<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseattribute">DRMGetUnboundLicenseAttribute</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseobject">DRMGetUnboundLicenseObject</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseobjectcount">DRMGetUnboundLicenseObjectCount</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/querying-licenses">Querying Licenses</a>
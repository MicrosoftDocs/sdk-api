---
UID: NF:msdrm.DRMGetUnboundLicenseAttribute
title: DRMGetUnboundLicenseAttribute function (msdrm.h)
description: Retrieves an unbound license attribute from the underlying XrML.
helpviewer_keywords: ["DRMGetUnboundLicenseAttribute","DRMGetUnboundLicenseAttribute function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetUnboundLicenseAttribute","rm.drmgetunboundlicenseattribute"]
old-location: rm\drmgetunboundlicenseattribute.htm
tech.root: rm
ms.assetid: 4ddf2920-95ea-47be-a5dd-b68eee2de29e
ms.date: 12/05/2018
ms.keywords: DRMGetUnboundLicenseAttribute, DRMGetUnboundLicenseAttribute function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetUnboundLicenseAttribute, rm.drmgetunboundlicenseattribute
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
 - DRMGetUnboundLicenseAttribute
 - msdrm/DRMGetUnboundLicenseAttribute
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
 - DRMGetUnboundLicenseAttribute
---

# DRMGetUnboundLicenseAttribute function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetUnboundLicenseAttribute</b> function retrieves an unbound license attribute from the underlying XrML.

## -parameters

### -param hQueryRoot [in]

A handle to a license or object in the license, created by using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseobject">DRMGetUnboundLicenseObject</a> or <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmparseunboundlicense">DRMParseUnboundLicense</a>.

### -param wszAttributeType [in]

Name of the attribute to retrieve.

### -param iWhich [in]

Zero-based index of the attribute to retrieve.

### -param peEncoding [out]

An enumeration value specifying the encoding type of the return value.

### -param pcBuffer [in, out]

Size of the returned data, in characters, plus one for a null terminator.

### -param pbBuffer [out]

Attribute value.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Attributes hold information about an object, such as its name, issue time, or SKU value. All allocating and freeing of memory are the responsibility of the caller. To obtain the size of the returned value, first call this function with the attribute sought (such as "Issue Date"), and <b>NULL</b> in the <i>pbBuffer</i> value. The size required for the buffer will be passed out in <i>pcBuffer</i>.

An object may have several instances of an attribute with the same name. For example, a <b>RIGHT</b> object may have several name-value pairs. In this case, it may be necessary to iterate through all the instances of an attribute (g_wszQUERY_RIGHTSPARAMETERNAME or g_wszQUERY_RIGHTSPARAMETERVALUE in the preceding example) by first calling <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseattributecount">DRMGetUnboundLicenseAttributeCount</a> to get a count of existing objects, and then looping through all <i>iWhich</i> instances of the attribute, starting at zero and incrementing by one.

This query will search only at the level immediately below the passed in object. So, for example, if the root license handle is passed in and the attribute to find is g_wszQUERY_SKUVALUE, the query will find nothing because the SKUVALUE appears at the second level or deeper (counting the license root as level 0).

The only attributes you can query for in an issuance license are g_wszQUERY_IDTYPE, g_wszQUERY_IDVALUE, g_wszQUERY_NAME, g_wszQUERY_ADDRESSTYPE, and g_wszQUERY_ADDRESSVALUE.

## -see-also

<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseattributecount">DRMGetUnboundLicenseAttributeCount</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseobject">DRMGetUnboundLicenseObject</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseobjectcount">DRMGetUnboundLicenseObjectCount</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/querying-licenses">Querying Licenses</a>
---
UID: NF:msdrm.DRMGetUnboundLicenseObjectCount
title: DRMGetUnboundLicenseObjectCount function (msdrm.h)
description: Counts the instances of an object within a specified branch of the license.
helpviewer_keywords: ["DRMGetUnboundLicenseObjectCount","DRMGetUnboundLicenseObjectCount function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetUnboundLicenseObjectCount","rm.drmgetunboundlicenseobjectcount"]
old-location: rm\drmgetunboundlicenseobjectcount.htm
tech.root: rm
ms.assetid: a1c2ae7e-a0be-482d-a366-70988cbc4616
ms.date: 12/05/2018
ms.keywords: DRMGetUnboundLicenseObjectCount, DRMGetUnboundLicenseObjectCount function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetUnboundLicenseObjectCount, rm.drmgetunboundlicenseobjectcount
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
 - DRMGetUnboundLicenseObjectCount
 - msdrm/DRMGetUnboundLicenseObjectCount
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
 - DRMGetUnboundLicenseObjectCount
---

# DRMGetUnboundLicenseObjectCount function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetUnboundLicenseObjectCount</b> function counts the instances of an object within a specified branch of the license.

## -parameters

### -param hQueryRoot [in]

A handle to a license or object in the license, created using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseobject">DRMGetUnboundLicenseObject</a> or <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmparseunboundlicense">DRMParseUnboundLicense</a>.

### -param wszSubObjectType [in]

The type of XrML object to find. For more information, see Remarks.

### -param pcSubObjects [out]

Count of object instances one level down within the specified branch.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Certain objects, such as rights, may have multiple instances in a license. This function allows an application to iterate through instances of an object type by providing an upper bound in a loop when calling <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseobject">DRMGetUnboundLicenseObject</a>. The value returned by this function, however, is one-based; subtract one from it when using it as a loop boundary.

This query will search only at the level immediately below the passed in object. So, for example, if the root license handle is passed in and the attribute to find is g_wszQUERY_OWNER, the query will find nothing because the OWNER appears at the second level or deeper (counting the license root as level 0).

## -see-also

<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseattribute">DRMGetUnboundLicenseAttribute</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseattributecount">DRMGetUnboundLicenseAttributeCount</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseobject">DRMGetUnboundLicenseObject</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/querying-licenses">Querying Licenses</a>
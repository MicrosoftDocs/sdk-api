---
UID: NF:msdrm.DRMDeleteLicense
title: DRMDeleteLicense function (msdrm.h)
description: Deletes a license, client licensor certificate, revocation list, or issuance license template.
helpviewer_keywords: ["DRMDeleteLicense","DRMDeleteLicense function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMDeleteLicense","rm.drmdeletelicense"]
old-location: rm\drmdeletelicense.htm
tech.root: rm
ms.assetid: 596f9959-0beb-4051-87c4-b8704abd8fc0
ms.date: 12/05/2018
ms.keywords: DRMDeleteLicense, DRMDeleteLicense function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMDeleteLicense, rm.drmdeletelicense
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
 - DRMDeleteLicense
 - msdrm/DRMDeleteLicense
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
 - DRMDeleteLicense
---

# DRMDeleteLicense function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMDeleteLicense</b> function deletes a license, client licensor certificate, revocation list, or issuance license template.

## -parameters

### -param hSession [in]

A handle to a license storage session or client session. You can use a  storage session handle to delete end-user licenses and revocation lists. You can use a client session handle to delete end-user licenses, rights account certificates,  client licensor certificates, and issuance license templates.

You can retrieve a handle to a license storage session by using   the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreatelicensestoragesession">DRMCreateLicenseStorageSession</a> function. You can retrieve a handle to a client session by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> function.

### -param wszLicenseId [in]

A pointer to a null-terminated string that contains the ID of the license or template to be deleted. The license ID can be found inside the <b>ID</b> element of the license XrML, by querying using the license querying functions and the <b>g_wszQUERY_CONTENTIDVALUE</b> constant. The template ID is a GUID. You can enumerate the GUIDs by calling the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a> function.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The AD RMS system does not check to determine whether out of date licenses or revocation lists are stored in the license store, even when acquiring a new license or revocation list for content already owned. Therefore, it is important to occasionally delete  licenses or certificates. This can be a time-consuming process, so it might be best to perform this action occasionally or during program idle time.

If you delete an <a href="/previous-versions/windows/desktop/adrms_sdk/e-gly">end-user license</a>, this function will not automatically delete associated revocation lists.

If you delete a license by using the content  ID, the <i>hSession</i> parameter must be the handle of a client session.

License and certificate IDs can be enumerated by using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a>. If you already have the license or certificate you want to delete from the license store, you can query it for its ID (by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmparseunboundlicense">DRMParseUnboundLicense</a> and <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseattribute">DRMGetUnboundLicenseAttribute</a> functions with the <b>g_wszQUERY_IDVALUE</b> constant) and pass the value into this function.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseattribute">DRMGetUnboundLicenseAttribute</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmparseunboundlicense">DRMParseUnboundLicense</a>
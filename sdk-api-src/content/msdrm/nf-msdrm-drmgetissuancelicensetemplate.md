---
UID: NF:msdrm.DRMGetIssuanceLicenseTemplate
title: DRMGetIssuanceLicenseTemplate function (msdrm.h)
description: Obtains an issuance license template from an existing issuance license.
helpviewer_keywords: ["DRMGetIssuanceLicenseTemplate","DRMGetIssuanceLicenseTemplate function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetIssuanceLicenseTemplate","rm.drmgetissuancelicensetemplate"]
old-location: rm\drmgetissuancelicensetemplate.htm
tech.root: rm
ms.assetid: 6667bab3-5022-4279-846a-61a0a37e9d33
ms.date: 12/05/2018
ms.keywords: DRMGetIssuanceLicenseTemplate, DRMGetIssuanceLicenseTemplate function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetIssuanceLicenseTemplate, rm.drmgetissuancelicensetemplate
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
 - DRMGetIssuanceLicenseTemplate
 - msdrm/DRMGetIssuanceLicenseTemplate
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
 - DRMGetIssuanceLicenseTemplate
---

# DRMGetIssuanceLicenseTemplate function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetIssuanceLicenseTemplate</b> function obtains an issuance license template from an existing issuance license.

## -parameters

### -param hIssuanceLicense [in]

The handle of the issuance license to create a template from.

### -param puIssuanceLicenseTemplateLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszIssuanceLicenseTemplate</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszIssuanceLicenseTemplate</i> buffer.

### -param wszIssuanceLicenseTemplate [out]

A pointer to a null-terminated Unicode string that receives the issuance license template XrML. The size of this buffer is specified by the <i>puIssuanceLicenseTemplateLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puIssuanceLicenseTemplateLength</i> value.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function is used to extract a XrML string version of an issuance license when you have a handle to an existing issuance license. This string can then be used as a template to create a new issuance license. To create a new template, first create a blank issuance license by calling <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateissuancelicense">DRMCreateIssuanceLicense</a> (working from a prior template or not), then add custom rights, users, or other information to the issuance license. Pass the modified issuance license to this function and extract the template.

Memory allocation and release for out parameters is the responsibility of the calling function. To obtain the size needed to hold the template string, call this function with <b>NULL</b> in the <i>wszIssuanceLicenseTemplate</i> parameter to retrieve the required size in the <i>puIssuanceLicenseTemplateLength</i> parameter.

The issuance license passed in to <b>DRMGetIssuanceLicenseTemplate</b> must have metadata and associated rights. If it does not, the function call will fail. Use the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetmetadata">DRMSetMetaData</a> function to set metadata for an issuance license. Use the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateright">DRMCreateRight</a> or <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmaddrightwithuser">DRMAddRightWithUser</a> functions to create or add rights.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateissuancelicense">DRMCreateIssuanceLicense</a>
---
UID: NF:msdrm.DRMGetNameAndDescription
title: DRMGetNameAndDescription function (msdrm.h)
description: Retrieves a language specific name and description from an issuance license.
helpviewer_keywords: ["DRMGetNameAndDescription","DRMGetNameAndDescription function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetNameAndDescription","rm.drmgetnameanddescription"]
old-location: rm\drmgetnameanddescription.htm
tech.root: rm
ms.assetid: 9e04ee69-bfec-456a-99ca-93e3158aeef9
ms.date: 12/05/2018
ms.keywords: DRMGetNameAndDescription, DRMGetNameAndDescription function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetNameAndDescription, rm.drmgetnameanddescription
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
 - DRMGetNameAndDescription
 - msdrm/DRMGetNameAndDescription
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
 - DRMGetNameAndDescription
---

# DRMGetNameAndDescription function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetNameAndDescription</b> function retrieves a language specific name and description from an issuance license.

## -parameters

### -param hIssuanceLicense [in]

A handle to the issuance license to get the information from.

### -param uIndex [in]

The zero-based index of the name and description pair to retrieve.

### -param pulcid [out]

A pointer to a <b>UINT</b> that receives the locale ID of the name and description pair.

### -param puNameLength [in, out]

A pointer to a <b>UINT</b> that, on input, contains the length, in characters, of the <i>wszName</i> buffer. This length must include the terminating null character.

After the function returns, this <b>UINT</b> contains the number of characters, including the terminating null character, that were copied to the <i>wszName</i> buffer.

### -param wszName [out]

A pointer to a null-terminated Unicode string that receives the name. The size of this buffer is specified by the <i>puNameLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puNameLength</i> parameter.

### -param puDescriptionLength [in, out]

A pointer to a <b>UINT</b> that, on input, contains the length, in characters, of the <i>wszDescription</i> buffer. This length must include the terminating null character.

After the function returns, this <b>UINT</b> contains the number of characters, including the terminating null character, that were copied to the <i>wszDescription</i> buffer.

### -param wszDescription [out]

A pointer to a null-terminated Unicode string that receives the description. The size of this buffer is specified by the <i>puDescriptionLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puDescriptionLength</i> parameter.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

<div class="alert"><b>Note</b>  If, when you enumerate through the Name/Description pairs for locales, you are unable to find the Name/Description pair corresponding with your locale (using the locale ID), you can use the LCID of 0, which is the  default value. Take note that an LCID of 0  can be set only for templates and licenses created programmatically on the client. AD RMS server administration does not support setting a default language for Name and Description. For more information about creating an issuance license programmatically, see   <a href="/previous-versions/windows/desktop/adrms_sdk/creating-an-issuance-license">Creating an Issuance License</a>.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetnameanddescription">DRMSetNameAndDescription</a>
---
UID: NF:slpublic.SLGetReferralInformation
title: SLGetReferralInformation function (slpublic.h)
description: Gets referral information for the specified product.
helpviewer_keywords: ["SLGetReferralInformation","SLGetReferralInformation function [Security]","SL_DOWNLOADURL","SL_INSTALLATIONPARAMETERS","SL_MERCHANTCOMMERCEURL","SL_MERCHANTSUPPORTEMAIL","SL_MERCHANTSUPPORTPHONENUMBER","SL_MERCHANTSUPPORTURL","SL_MERCHANTUPGRADEURL","SL_PARTNERID","SL_REFERRALID","SL_SERIALIZEDDATA","security.slgetreferralinformation","slpublic/SLGetReferralInformation"]
old-location: security\slgetreferralinformation.htm
tech.root: security
ms.assetid: 880ee26d-4deb-415c-b1dd-f17d802ea8e8
ms.date: 12/05/2018
ms.keywords: SLGetReferralInformation, SLGetReferralInformation function [Security], SL_DOWNLOADURL, SL_INSTALLATIONPARAMETERS, SL_MERCHANTCOMMERCEURL, SL_MERCHANTSUPPORTEMAIL, SL_MERCHANTSUPPORTPHONENUMBER, SL_MERCHANTSUPPORTURL, SL_MERCHANTUPGRADEURL, SL_PARTNERID, SL_REFERRALID, SL_SERIALIZEDDATA, security.slgetreferralinformation, slpublic/SLGetReferralInformation
req.header: slpublic.h
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
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SLGetReferralInformation
 - slpublic/SLGetReferralInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Slc.dll
api_name:
 - SLGetReferralInformation
---

# SLGetReferralInformation function


## -description

Gets referral information for the specified product.

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

The handle retrieved by previous call to the <a href="/windows/desktop/api/slpublic/nf-slpublic-slopen">SLOpen</a> function.

### -param eReferralType [in]

Type: <b><a href="/windows/desktop/api/slpublic/ne-slpublic-slreferraltype">SLREFERRALTYPE</a></b>

The referral type.

### -param pSkuOrAppId [in]

Type: <b>const SLID*</b>

A pointer to the <b>SLID</b> of the application or SKU from which to obtain information.

### -param pwszValueName [in]

Type: <b>PCWSTR</b>

The name associated with the value to retrieve.  The following names are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SL_PARTNERID"></a><a id="sl_partnerid"></a><dl>
<dt><b>SL_PARTNERID</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Partner ID for the license reseller

</td>
</tr>
<tr>
<td width="40%"><a id="SL_REFERRALID"></a><a id="sl_referralid"></a><dl>
<dt><b>SL_REFERRALID</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Referral ID for the license reseller

</td>
</tr>
<tr>
<td width="40%"><a id="SL_MERCHANTCOMMERCEURL"></a><a id="sl_merchantcommerceurl"></a><dl>
<dt><b>SL_MERCHANTCOMMERCEURL</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The merchant URL to purchase additional licenses

</td>
</tr>
<tr>
<td width="40%"><a id="SL_MERCHANTUPGRADEURL"></a><a id="sl_merchantupgradeurl"></a><dl>
<dt><b>SL_MERCHANTUPGRADEURL</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The merchant URL to purchase additional licenses

</td>
</tr>
<tr>
<td width="40%"><a id="SL_DOWNLOADURL"></a><a id="sl_downloadurl"></a><dl>
<dt><b>SL_DOWNLOADURL</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
A forward link to download the associated application

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INSTALLATIONPARAMETERS"></a><a id="sl_installationparameters"></a><dl>
<dt><b>SL_INSTALLATIONPARAMETERS</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Any parameters that are used when running the associated application's installer

</td>
</tr>
<tr>
<td width="40%"><a id="SL_MERCHANTSUPPORTPHONENUMBER"></a><a id="sl_merchantsupportphonenumber"></a><dl>
<dt><b>SL_MERCHANTSUPPORTPHONENUMBER</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The merchant support phone number(s)

</td>
</tr>
<tr>
<td width="40%"><a id="SL_MERCHANTSUPPORTEMAIL"></a><a id="sl_merchantsupportemail"></a><dl>
<dt><b>SL_MERCHANTSUPPORTEMAIL</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The merchant support email address

</td>
</tr>
<tr>
<td width="40%"><a id="SL_MERCHANTSUPPORTURL"></a><a id="sl_merchantsupporturl"></a><dl>
<dt><b>SL_MERCHANTSUPPORTURL</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The merchant support URL

</td>
</tr>
<tr>
<td width="40%"><a id="SL_SERIALIZEDDATA"></a><a id="sl_serializeddata"></a><dl>
<dt><b>SL_SERIALIZEDDATA</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
A generic data BLOB

</td>
</tr>
</table>

### -param ppwszValue [out]

Type: <b>PWSTR*</b>

The value to store. When finished using the memory, free it by calling the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

## -returns

Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise,  it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
</table>
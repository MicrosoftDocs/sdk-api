---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# SLGetReferralInformation function


## -description


Gets referral information for the specified product.


## -parameters




### -param hSLC [in]

Type: <b>HSLC</b>

The handle retrieved by previous call to the <a href="https://msdn.microsoft.com/79a09cf3-cf6f-479a-89c7-27f5fcee3186">SLOpen</a> function.


### -param eReferralType [in]

Type: <b><a href="https://msdn.microsoft.com/350a28bd-cbdf-46f2-a404-aa16550a4711">SLREFERRALTYPE</a></b>

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

The value to store. When finished using the memory, free it by calling the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


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
 




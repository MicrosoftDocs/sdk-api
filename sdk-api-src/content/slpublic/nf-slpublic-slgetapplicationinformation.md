---
UID: NF:slpublic.SLGetApplicationInformation
title: SLGetApplicationInformation function (slpublic.h)
description: Gets information about the specified application.
helpviewer_keywords: ["SLGetApplicationInformation","SLGetApplicationInformation function [Security]","SL_DATA_BINARY","SL_DATA_DWORD","SL_DATA_SZ","SL_INFO_KEY_IS_KMS","SL_INFO_KEY_KMS_CURRENT_COUNT","SL_INFO_KEY_KMS_FAILED_REQUESTS","SL_INFO_KEY_KMS_LICENSED_REQUESTS","SL_INFO_KEY_KMS_NON_GENUINE_GRACE_REQUESTS","SL_INFO_KEY_KMS_NOTIFICATION_REQUESTS","SL_INFO_KEY_KMS_OOB_GRACE_REQUESTS","SL_INFO_KEY_KMS_OOT_GRACE_REQUESTS","SL_INFO_KEY_KMS_REQUIRED_CLIENT_COUNT","SL_INFO_KEY_KMS_TOTAL_REQUESTS","SL_INFO_KEY_KMS_UNLICENSED_REQUESTS","security.slgetapplicationinformation","slpublic/SLGetApplicationInformation"]
old-location: security\slgetapplicationinformation.htm
tech.root: security
ms.assetid: f745e1e1-74c8-4563-9c29-d3184d8d4f6d
ms.date: 12/05/2018
ms.keywords: SLGetApplicationInformation, SLGetApplicationInformation function [Security], SL_DATA_BINARY, SL_DATA_DWORD, SL_DATA_SZ, SL_INFO_KEY_IS_KMS, SL_INFO_KEY_KMS_CURRENT_COUNT, SL_INFO_KEY_KMS_FAILED_REQUESTS, SL_INFO_KEY_KMS_LICENSED_REQUESTS, SL_INFO_KEY_KMS_NON_GENUINE_GRACE_REQUESTS, SL_INFO_KEY_KMS_NOTIFICATION_REQUESTS, SL_INFO_KEY_KMS_OOB_GRACE_REQUESTS, SL_INFO_KEY_KMS_OOT_GRACE_REQUESTS, SL_INFO_KEY_KMS_REQUIRED_CLIENT_COUNT, SL_INFO_KEY_KMS_TOTAL_REQUESTS, SL_INFO_KEY_KMS_UNLICENSED_REQUESTS, security.slgetapplicationinformation, slpublic/SLGetApplicationInformation
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
 - SLGetApplicationInformation
 - slpublic/SLGetApplicationInformation
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
 - SLGetApplicationInformation
---

# SLGetApplicationInformation function


## -description

Gets information about the specified application.

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.

### -param pApplicationId [in]

Type: <b>const SLID*</b>

A pointer to the application ID.

### -param pwszValueName [in]

Type: <b>PCWSTR</b>

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_IS_KMS"></a><a id="sl_info_key_is_kms"></a><dl>
<dt><b>SL_INFO_KEY_IS_KMS</b></dt>
<dt>L"IsKeyManagementService"</dt>
</dl>
</td>
<td width="60%">
Indicates whether the machine has a Key Management Service (KMS) enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_KMS_CURRENT_COUNT"></a><a id="sl_info_key_kms_current_count"></a><dl>
<dt><b>SL_INFO_KEY_KMS_CURRENT_COUNT</b></dt>
<dt>L"KeyManagementServiceCurrentCount" </dt>
</dl>
</td>
<td width="60%">
The number of volume clients on a KMS host that are currently active.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_KMS_REQUIRED_CLIENT_COUNT"></a><a id="sl_info_key_kms_required_client_count"></a><dl>
<dt><b>SL_INFO_KEY_KMS_REQUIRED_CLIENT_COUNT</b></dt>
<dt>L"KeyManagementServiceRequiredClientCount"</dt>
</dl>
</td>
<td width="60%">
The minimum number of VL clients required to connect to a KMS host for enabling activation.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_KMS_UNLICENSED_REQUESTS"></a><a id="sl_info_key_kms_unlicensed_requests"></a><dl>
<dt><b>SL_INFO_KEY_KMS_UNLICENSED_REQUESTS</b></dt>
<dt>L"KeyManagementServiceUnlicensedRequests"</dt>
</dl>
</td>
<td width="60%">
The number of KMS requests from VL clients with License Status=Unlicensed.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_KMS_LICENSED_REQUESTS"></a><a id="sl_info_key_kms_licensed_requests"></a><dl>
<dt><b>SL_INFO_KEY_KMS_LICENSED_REQUESTS</b></dt>
<dt>L"KeyManagementServiceLicensedRequests"</dt>
</dl>
</td>
<td width="60%">
The number of KMS requests from VL clients with License Status=Licensed.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_KMS_OOB_GRACE_REQUESTS"></a><a id="sl_info_key_kms_oob_grace_requests"></a><dl>
<dt><b>SL_INFO_KEY_KMS_OOB_GRACE_REQUESTS</b></dt>
<dt>L"KeyManagementServiceOOBGraceRequests"</dt>
</dl>
</td>
<td width="60%">
The number of KMS requests from VL clients with License Status=OOB Grace.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_KMS_OOT_GRACE_REQUESTS"></a><a id="sl_info_key_kms_oot_grace_requests"></a><dl>
<dt><b>SL_INFO_KEY_KMS_OOT_GRACE_REQUESTS</b></dt>
<dt>L"KeyManagementServiceOOTGraceRequests"</dt>
</dl>
</td>
<td width="60%">
The number of KMS requests from VL clients with License Status=OOT Grace.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_KMS_NON_GENUINE_GRACE_REQUESTS"></a><a id="sl_info_key_kms_non_genuine_grace_requests"></a><dl>
<dt><b>SL_INFO_KEY_KMS_NON_GENUINE_GRACE_REQUESTS</b></dt>
<dt>L"KeyManagementServiceNonGenuineGraceRequests"</dt>
</dl>
</td>
<td width="60%">
The number of KMS requests from VL clients with License Status=Non-Genuine Grace.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_KMS_NOTIFICATION_REQUESTS"></a><a id="sl_info_key_kms_notification_requests"></a><dl>
<dt><b>SL_INFO_KEY_KMS_NOTIFICATION_REQUESTS</b></dt>
<dt>L"KeyManagementServiceNotificationRequests"</dt>
</dl>
</td>
<td width="60%">
The number of KMS requests from VL clients with License Status=Notification.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_KMS_TOTAL_REQUESTS"></a><a id="sl_info_key_kms_total_requests"></a><dl>
<dt><b>SL_INFO_KEY_KMS_TOTAL_REQUESTS</b></dt>
<dt>L"KeyManagementServiceTotalRequests"</dt>
</dl>
</td>
<td width="60%">
Total number of valid KMS requests.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_INFO_KEY_KMS_FAILED_REQUESTS"></a><a id="sl_info_key_kms_failed_requests"></a><dl>
<dt><b>SL_INFO_KEY_KMS_FAILED_REQUESTS</b></dt>
<dt>L"KeyManagementServiceFailedRequests"</dt>
</dl>
</td>
<td width="60%">
Total number of failed KMS requests.

</td>
</tr>
</table>

### -param peDataType [out, optional]

Type: <b><a href="/windows/desktop/api/slpublic/ne-slpublic-sldatatype">SLDATATYPE</a>*</b>

A pointer to a value of the <a href="/windows/desktop/api/slpublic/ne-slpublic-sldatatype">SLDATATYPE</a> enumeration that specifies the type of data in the ppbValue buffer.  The following values are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SL_DATA_SZ"></a><a id="sl_data_sz"></a><dl>
<dt><b>SL_DATA_SZ</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
UNICODE string

</td>
</tr>
<tr>
<td width="40%"><a id="SL_DATA_DWORD"></a><a id="sl_data_dword"></a><dl>
<dt><b>SL_DATA_DWORD</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
DWORD

</td>
</tr>
<tr>
<td width="40%"><a id="SL_DATA_BINARY"></a><a id="sl_data_binary"></a><dl>
<dt><b>SL_DATA_BINARY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Binary blob

</td>
</tr>
</table>

### -param pcbValue [out]

Type: <b>UINT*</b>

A pointer to the size, in bytes, of the <i>ppbValue</i> buffer.

### -param ppbValue [out]

Type: <b>PBYTE*</b>

If successful, the data is returned in the buffer allocated by the SLC.       
		When finished using the memory, free it by calling the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

## -returns

Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise, it returns an <b>HRESULT</b> error code.

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
One or more arguments are  not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_VALUE_NOT_FOUND</b></dt>
<dt>0xC004F012</dt>
</dl>
</td>
<td width="60%">
The value for the input key was not found.

</td>
</tr>
</table>
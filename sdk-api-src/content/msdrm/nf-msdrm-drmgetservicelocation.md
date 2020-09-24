---
UID: NF:msdrm.DRMGetServiceLocation
title: DRMGetServiceLocation function (msdrm.h)
description: Retrieves the URL of a server that can perform various rights management services, such as activation or license acquisition.
helpviewer_keywords: ["DRMGetServiceLocation","DRMGetServiceLocation function [Active Directory Rights Management Services SDK 1.0]","DRM_SERVICE_LOCATION_ENTERPRISE","DRM_SERVICE_LOCATION_INTERNET","DRM_SERVICE_TYPE_ACTIVATION","DRM_SERVICE_TYPE_CERTIFICATION","DRM_SERVICE_TYPE_CLIENTLICENSOR","DRM_SERVICE_TYPE_PUBLISHING","DRM_SERVICE_TYPE_SILENT","msdrm/DRMGetServiceLocation","rm.drmgetservicelocation"]
old-location: rm\drmgetservicelocation.htm
tech.root: rm
ms.assetid: f7cbc3ba-009f-4a35-999e-139d41961fd9
ms.date: 12/05/2018
ms.keywords: DRMGetServiceLocation, DRMGetServiceLocation function [Active Directory Rights Management Services SDK 1.0], DRM_SERVICE_LOCATION_ENTERPRISE, DRM_SERVICE_LOCATION_INTERNET, DRM_SERVICE_TYPE_ACTIVATION, DRM_SERVICE_TYPE_CERTIFICATION, DRM_SERVICE_TYPE_CLIENTLICENSOR, DRM_SERVICE_TYPE_PUBLISHING, DRM_SERVICE_TYPE_SILENT, msdrm/DRMGetServiceLocation, rm.drmgetservicelocation
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
 - DRMGetServiceLocation
 - msdrm/DRMGetServiceLocation
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
 - DRMGetServiceLocation
---

# DRMGetServiceLocation function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetServiceLocation</b> function retrieves the URL of a server that can perform various rights management services, such as activation or license acquisition.

## -parameters

### -param hClient [in, optional]

A handle to a client session. The handle can be obtained by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> function. The handle is optional and can be <b>NULL</b>.

### -param uServiceType [in]

Specifies the type of service desired. This can be one of the following values.



#### DRM_SERVICE_TYPE_ACTIVATION

Retrieve the computer activation service.



#### DRM_SERVICE_TYPE_CERTIFICATION

Retrieve the <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificate</a> service.



#### DRM_SERVICE_TYPE_CLIENTLICENSOR

Retrieve the <a href="/previous-versions/windows/desktop/adrms_sdk/c-gly">client licensor certificates</a> service (for offline publishing).



#### DRM_SERVICE_TYPE_PUBLISHING

Retrieve the <a href="/previous-versions/windows/desktop/adrms_sdk/i-gly">issuance license</a> signing service (for online publishing).



#### DRM_SERVICE_TYPE_SILENT

Suppresses the appearance of any user-interface dialog boxes when the request is made to retrieve the service location.

### -param uServiceLocation [in]

Specifies where to find the AD RMS server. This can be one of the following values.



#### DRM_SERVICE_LOCATION_ENTERPRISE

Look within the enterprise for an AD RMS server.



#### DRM_SERVICE_LOCATION_INTERNET

Look on the Internet for an AD RMS server.

### -param wszIssuanceLicense [in]

A pointer to a null-terminated Unicode string that contains a signed issuance license. This parameter can be <b>NULL</b>. For more information, see Remarks.

### -param puServiceURLLength [in, out]

A pointer to a <b>UINT</b> that, on input, contains the size, in characters, of the <i>wszServiceURL</i> buffer. This value includes the terminating null character.

After the function returns, this <b>UINT</b> contains the number of characters, including the terminating null character, that were copied to the <i>wszServiceURL</i> buffer.

If <i>wszServiceURL</i> is <b>NULL</b>, this <b>UINT</b> receives the number of characters, including the terminating null character, that are required for the server URL.

### -param wszServiceURL [out]

A pointer to a Unicode string buffer that receives the URL of the server. The <i>puServiceURLLength</i> parameter contains the size, in characters, including the terminating null character, of this buffer.

If this parameter is <b>NULL</b>, <i>puServiceURLLength</i> receives the number of characters, including the terminating null character, that are required for the server URL.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Discovery of the service URL depends on the interaction between the <i>uServiceType</i>, <i>uServiceLocation</i>, and <i>wszIssuanceLicense</i> parameters in the following manner.

If you set the <i>uServiceType</i> parameter to DRM_SERVICE_TYPE_CERTIFICATION or to  DRM_SERVICE_TYPE_ACTIVATION and:<ul>
<li>You pass a signed issuance license to the <i>wszIssuanceLicense</i> parameter. The licensing URL is retrieved from the signed issuance license, a call is made to the licensing server to discover the certification URL that corresponds with the calling user, and the function returns the certification URL.</li>
<li>You set the <i>wszIssuanceLicense</i> parameter to <b>NULL</b> and the <i>uServiceLocation</i> parameter to DRM_SERVICE_LOCATION_INTERNET, the function returns an error code of E_DRM_USE_DEFAULT.</li>
<li>You set the <i>wszIssuanceLicense</i> parameter to <b>NULL</b>, and the  <i>uServiceLocation</i> parameter to DRM_SERVICE_LOCATION_ENTERPRISE, the URL is retrieved from the registry or from Active Directory (AD).</li>
</ul>


If you set the <i>uServiceType</i> parameter to DRM_SERVICE_TYPE_PUBLISHING or to DRM_SERVICE_TYPE_CLIENTLICENSOR and:<ul>
<li>You set the <i>uServiceLocation</i> parameter to DRM_SERVICE_LOCATION_INTERNET, the Passport service is supported to retrieve a service URL from the web.</li>
<li>You set the  <i>uServiceLocation</i> parameter to DRM_SERVICE_LOCATION_ENTERPRISE and the <i>wszIssuanceLicense</i> parameter to <b>NULL</b>, the licensing service URL is retrieved from the registry and returned by the function call. Or, in the absence of a registry entry, the certification URL is retrieved from the service connection point in Active Directory (AD), a call is made to the certification server to discover the licensing service URL, and the function returns the licensing service URL.</li>
<li>You set the  <i>uServiceLocation</i> parameter to DRM_SERVICE_LOCATION_ENTERPRISE and pass a signed issuance license to the <i>wszIssuanceLicense</i> parameter, the function attempts to retrieve the configured licensing URL from the registry. If this attempt fails, the licensing URL is retrieved from the signed issuance license and a call is made to the licensing server to discover the user's specific licensing URL.</li>
</ul>


For the preceding cases where the function searches the registry, you can force your application to find a specific URL by adding the appropriate registry key in the following list, along with the URL, as a string value called <b>(default)</b>.  Do not add the .asmx page to the URL.<table>
<tr>
<th>Registry key</th>
<th>Description</th>
</tr>
<tr>
<td>
<ul>
<li>32-bit application on a 32-bit computer</li>
<li>64-bit application on a 64-bit computer</li>
</ul>
<b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b>&#92;<b>MSDRM</b>&#92;<b>ServiceLocation</b>&#92;<b>Activation</b>

<ul>
<li>32-bit application on a 64-bit computer</li>
</ul>
<b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Wow6432Node</b>&#92;<b>Microsoft</b>&#92;<b>MSDRM</b>&#92;<b>ServiceLocation</b>&#92;<b>Activation</b>

</td>
<td>
For RMS v1.0, set this registry value to the URL of a computer activation service. To use this value for certification, set it to the certification virtual root of the enterprise.

Beginning with RMS v1.0 SP1, this value can only be used to discover a certification service. Therefore, set it to the URL of the rights account virtual root, http://<i>ServerName</i>/_wmcs/certification.

</td>
</tr>
<tr>
<td>
<ul>
<li>32-bit application on a 32-bit computer</li>
<li>64-bit application on a 64-bit computer</li>
</ul>
<b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b>&#92;<b>MSDRM</b>&#92;<b>ServiceLocation</b>&#92;<b>EnterprisePublishing</b>

<ul>
<li>32-bit application on a 64-bit computer</li>
</ul>
<b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Wow6432Node</b>&#92;<b>Microsoft</b>&#92;<b>MSDRM</b>&#92;<b>ServiceLocation</b>&#92;<b>EnterprisePublishing</b>

</td>
<td>Set this registry value to the URL of a service that signs issuance licenses within an enterprise network.</td>
</tr>
<tr>
<td>
<ul>
<li>32-bit application on a 32-bit computer</li>
<li>64-bit application on a 64-bit computer</li>
</ul>
<b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b>&#92;<b>MSDRM</b>&#92;<b>ServiceLocation</b>&#92;<b>CloudPublishing</b>

<ul>
<li>32-bit application on a 64-bit computer</li>
</ul>
<b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Wow6432Node</b>&#92;<b>Microsoft</b>&#92;<b>MSDRM</b>&#92;<b>ServiceLocation</b>&#92;<b>CloudPublishing</b>

</td>
<td>Set this registry value to the URL of a service that signs issuance licenses over the Internet.</td>
</tr>
</table>
 



The application is responsible for allocating and freeing memory for the retrieved data. To find the buffer size required, call the function with <b>NULL</b> in the <i>wszServiceURL</i> parameter. The buffer size will be passed back to you  through the <i>puServiceURLLength</i> parameter.

For a service discovery code example, see <a href="/previous-versions/windows/desktop/adrms_sdk/onlinesigning-getserviceurl-cpp">OnlineSigning_GetServiceURL.cpp</a>. There is no service discovery for acquiring <a href="/previous-versions/windows/desktop/adrms_sdk/e-gly">end-user licenses</a> because this information can be stored in the <a href="/previous-versions/windows/desktop/adrms_sdk/i-gly">issuance license</a> used to acquire the <i>end-user license</i>.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmactivate">DRMActivate</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/onlinesigning-getserviceurl-cpp">OnlineSigning_GetServiceURL.cpp</a>
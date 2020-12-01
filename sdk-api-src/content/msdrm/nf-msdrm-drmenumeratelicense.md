---
UID: NF:msdrm.DRMEnumerateLicense
title: DRMEnumerateLicense function (msdrm.h)
description: Enumerates valid licenses, machine certificates or rights account certificates, revocation lists for the current user, or issuance license templates.
helpviewer_keywords: ["DRMEnumerateLicense","DRMEnumerateLicense function [Active Directory Rights Management Services SDK 1.0]","DRM_EL_CLIENTLICENSOR","DRM_EL_CLIENTLICENSOR_LID","DRM_EL_EUL","DRM_EL_EUL_LID","DRM_EL_EXPIRED","DRM_EL_GROUPIDENTITY","DRM_EL_GROUPIDENTITY_LID","DRM_EL_GROUPIDENTITY_NAME","DRM_EL_ISSUANCELICENSE_TEMPLATE","DRM_EL_ISSUANCELICENSE_TEMPLATE_LID","DRM_EL_ISSUERNAME","DRM_EL_MACHINE","DRM_EL_REVOCATIONLIST","DRM_EL_REVOCATIONLIST_LID","DRM_EL_SPECIFIED_CLIENTLICENSOR","DRM_EL_SPECIFIED_GROUPIDENTITY","msdrm/DRMEnumerateLicense","rm.drmenumeratelicense"]
old-location: rm\drmenumeratelicense.htm
tech.root: rm
ms.assetid: 7a7797f2-d219-4a17-ac3d-96134cd14a55
ms.date: 12/05/2018
ms.keywords: DRMEnumerateLicense, DRMEnumerateLicense function [Active Directory Rights Management Services SDK 1.0], DRM_EL_CLIENTLICENSOR, DRM_EL_CLIENTLICENSOR_LID, DRM_EL_EUL, DRM_EL_EUL_LID, DRM_EL_EXPIRED, DRM_EL_GROUPIDENTITY, DRM_EL_GROUPIDENTITY_LID, DRM_EL_GROUPIDENTITY_NAME, DRM_EL_ISSUANCELICENSE_TEMPLATE, DRM_EL_ISSUANCELICENSE_TEMPLATE_LID, DRM_EL_ISSUERNAME, DRM_EL_MACHINE, DRM_EL_REVOCATIONLIST, DRM_EL_REVOCATIONLIST_LID, DRM_EL_SPECIFIED_CLIENTLICENSOR, DRM_EL_SPECIFIED_GROUPIDENTITY, msdrm/DRMEnumerateLicense, rm.drmenumeratelicense
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
 - DRMEnumerateLicense
 - msdrm/DRMEnumerateLicense
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
 - DRMEnumerateLicense
---

# DRMEnumerateLicense function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMEnumerateLicense</b> function enumerates valid licenses, <a href="/previous-versions/windows/desktop/adrms_sdk/m-gly">machine certificates</a> or <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificates</a>, <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">revocation lists</a> for the current user, or issuance license templates.

## -parameters

### -param hSession [in]

A handle to a client or license storage session. The type of session passed into <i>hSession</i> depends on the type of item to enumerate. To enumerate <a href="/previous-versions/windows/desktop/adrms_sdk/e-gly">end-user licenses</a>, use a license storage session created by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreatelicensestoragesession">DRMCreateLicenseStorageSession</a> function. To enumerate <a href="/previous-versions/windows/desktop/adrms_sdk/m-gly">machine certificates</a>, <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificates</a>, <a href="/previous-versions/windows/desktop/adrms_sdk/c-gly">client licensor certificates</a>, or issuance license templates, use a client session created by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> function. Use either type of handle to enumerate <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">revocation lists</a>.

### -param uFlags [in]

Contains one or more of the following values that specifies which types of items to enumerate and other options.


The following flag can be combined with other flags to specify additional enumeration options.





#### DRM_EL_EXPIRED

Use this value with flags used to enumerate identifiers, such as <b>DRM_EL_GROUPIDENTITY_LID</b>, to enumerate expired items of the specified type. This simplifies deleting expired items from the license store, keeping the store small and improving performance.


The following flags are used to enumerate <a href="/previous-versions/windows/desktop/adrms_sdk/e-gly">end-user licenses</a>.





#### DRM_EL_EUL

Enumerate <a href="/previous-versions/windows/desktop/adrms_sdk/e-gly">end-user licenses</a> for the current license storage session.



#### DRM_EL_EUL_LID

Enumerate <a href="/previous-versions/windows/desktop/adrms_sdk/e-gly">end-user license</a> identifiers for the current license storage session. The identifier of each <i>end-user license</i> is returned in the <i>wszCertificateData</i> parameter.


The following flags are used to enumerate <a href="/previous-versions/windows/desktop/adrms_sdk/c-gly">client licensor certificates</a>. These flags allow an application to enumerate through licensors in licenses available to the current user.





#### DRM_EL_CLIENTLICENSOR

Enumerate all <a href="/previous-versions/windows/desktop/adrms_sdk/c-gly">client licensor certificates</a> in the certificate store.



#### DRM_EL_CLIENTLICENSOR_LID

Enumerate <a href="/previous-versions/windows/desktop/adrms_sdk/c-gly">client licensor certificates</a> identifiers for the client session passed in. The client licensor certificate identifier is returned in the <i>wszCertificateData</i> parameter.



#### DRM_EL_SPECIFIED_CLIENTLICENSOR

Return the <a href="/previous-versions/windows/desktop/adrms_sdk/c-gly">client licensor certificate</a> that corresponds to the email address in the client session.


The following flag is  used to enumerate <a href="/previous-versions/windows/desktop/adrms_sdk/m-gly">machine certificates</a>.





#### DRM_EL_MACHINE

Enumerate the selected <a href="/previous-versions/windows/desktop/adrms_sdk/m-gly">machine certificate</a>. 

Each user has  two machine certificates. The valid index value for machine certificates is zero or one.

<div class="alert"><b>Note</b>  Due to updates to enable cryptographic mode-2, DRMActivate(machine) will write two machine certificates to the store. Unless an application makes direct calls to the certification web method on the RMS server, the calling application does not need to distinguish between the two machine certificates; the machine certificate that corresponds to the server cryptographic mode will be used.<p class="note">For more information, see <a href="https://support.microsoft.com/help/2627273">RSA key length is increased to 2048 bits for AD RMS in Windows 7 or in Windows Server 2008 R2</a>.

</div>
<div> </div>
If  <i>hSession</i> was created by a call to <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a>, the returned certificate is from the per-user certificate store and the value pointed to by <i>pfSharedFlag</i> is set to <b>FALSE</b>. If  <i>hSession</i> was created by a call to <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreatelicensestoragesession">DRMCreateLicenseStorageSession</a>, the value pointed to by <i>pfSharedFlag</i> is its original value.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 with SP2, Windows Vista with SP2 or Rights Management Services 1.0:  </b>For Rights Management Services 1.0, the retrieved certificate is from the machine store and the value pointed to by <i>pfSharedFlag</i> is set to <b>TRUE</b>; <i>uIndex</i> must be set to zero.

The machine must be activated before specifying this flag. If the machine is not activated, the function will return <b>E_DRM_NEEDS_MACHINE_ACTIVATION</b>.


The following flags are used to enumerate <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificates</a>.





#### DRM_EL_GROUPIDENTITY

Enumerate the <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificates</a> for the currently logged-in user. This includes both shared and restricted users.



#### DRM_EL_GROUPIDENTITY_LID

Enumerate the <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificates</a> identifiers for the currently logged-in user. This includes both shared and restricted users. The <i>rights account certificates</i> identifier will be returned in the <i>wszCertificateData</i> parameter.



#### DRM_EL_GROUPIDENTITY_NAME

Enumerate the rights account names for the current user.



#### DRM_EL_SPECIFIED_GROUPIDENTITY

Return the <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificates</a> for the specified user when the client session was created by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> function.


The following flags are used to enumerate <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">revocation lists</a>.

All certificates can include <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">revocation lists</a>, so you can pass in either a client or license storage session to this function. A client session handle passed in will retrieve <i>revocation lists</i> for <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificates</a> or <a href="/previous-versions/windows/desktop/adrms_sdk/c-gly">client licensor certificates</a>. A license storage session handle passed in will retrieve <i>revocation lists</i> for <a href="/previous-versions/windows/desktop/adrms_sdk/e-gly">end-user licenses</a>.





#### DRM_EL_REVOCATIONLIST

Enumerate <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">revocation lists</a>.



#### DRM_EL_REVOCATIONLIST_LID

Enumerate <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">revocation list</a> identifiers. The revocation list identifier will be returned in the <i>wszCertificateData</i> parameter.


The following flag can be used to retrieve the display name of the issuer.





#### DRM_EL_ISSUERNAME

This flag cannot be used with the <b>DRM_EL_EXPIRED</b> flag, and it must be used with one of the following flags:

<ul>
<li><b>DRM_EL_CLIENTLICENSOR</b></li>
<li><b>DRM_EL_GROUPIDENTITY</b></li>
<li><b>DRM_EL_SPECIFIED_CLIENTLICENSOR</b></li>
<li><b>DRM_EL_SPECIFIED_GROUPIDENTITY</b></li>
</ul>

The following flags can be used to enumerate templates.





#### DRM_EL_ISSUANCELICENSE_TEMPLATE

Enumerate issuance license templates. This flag is available beginning with Windows Vista with SP1 and Windows Server 2008.



#### DRM_EL_ISSUANCELICENSE_TEMPLATE_LID

Enumerate issuance license template identifiers (GUIDs). This flag is available beginning with Windows Vista with SP1 and Windows Server 2008.

### -param uIndex [in]

The index number of the certificate or license to retrieve. To begin an enumeration, pass in zero for this parameter. To obtain subsequent licenses, increment this value until the function returns <b>E_DRM_NO_MORE_DATA</b>. For more information, see Remarks.

### -param pfSharedFlag [in, out]

A pointer to a <b>BOOL</b> value that receives one (1) if the retrieved license is shared or zero (0) if the retrieved license is not shared.

### -param puCertificateDataLen [in, out]

A pointer to a UINT value that, on entry, contains the size of the <i>wszCertificateData</i> buffer. This size includes the terminating null character. After the function returns, this value contains the number of characters copied to the buffer, including the terminating null character.

To obtain the necessary size of the buffer, pass <b>NULL</b> for <i>wszCertificateData</i>. The required number of characters, including the terminating null character, will be placed in this value.

### -param wszCertificateData [out]

A pointer to  a null-terminated Unicode string that receives the license, ID, or template depending on which flags were 
set.

To obtain the necessary size of this buffer, pass <b>NULL</b> for <i>wszCertificateData</i>. The required number of characters, including the terminating null character, will be placed in <i>puCertificateDataLen</i>.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

By default, this function enumerates only unexpired licenses as determined by comparing the <b>VALIDITYTIME</b> element in each license with the creation time of the session object. To include expired licenses in the enumeration, combine the <i>uFlags</i> parameter with <b>DRM_EL_EXPIRED</b>.

Also, if the <b>ID</b> element in the <b>ISSUEDPRINCIPALS</b> element of the license does not match the user ID associated with the session object, or the session user ID does not match the ID of the logged–on user, this function will fail. For more information, see <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a>.

The following sections discuss how to enumerate the various types of licenses. When iterating through a collection, you can examine each license retrieved by manually parsing the XrML string or, in some cases, by binding to the license and using the <b>DRMGetBoundLicense*</b> functions.


Perform the following steps to enumerate an end-user license:

<ol>
<li>Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreatelicensestoragesession">DRMCreateLicenseStorageSession</a>, passing in a signed issuance license.</li>
<li>Set the <i>uIndex</i> parameter to zero and the  <i>uFlags</i> parameter to <b>DRM_EL_EUL</b> and call <b>DRMEnumerateLicense</b>. The AD RMS client retrieves the first valid EUL for which the content ID matches the content ID of the issuance license used to create the license storage session. If, however, the issuance license was republished with the same content ID but different rights, the EUL returned may not be the one sought. If it is not, increment the <i>uIndex</i> parameter and call <b>DRMEnumerateLicense</b> again. You can continue iterating until you find the correct EUL or the function returns  <b>E_DRM_NO_MORE_DATA</b>.</li>
</ol>


Perform the following steps to enumerate a machine certificate:<ol>
<li>Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> or <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreatelicensestoragesession">DRMCreateLicenseStorageSession</a> to create a session object. The type of session created determines the nature of the value returned in the <i>pfSharedFlag</i> parameter. For more information, see the <b>DRM_EL_MACHINE</b> constant in the <i>uFlags</i> parameter.</li>
<li>Set the <i>uIndex</i> parameter to zero or one and the  <i>uFlags</i> parameter to <b>DRM_EL_MACHINE</b> and call <b>DRMEnumerateLicense</b>.</li>
</ol>


Perform the following steps to enumerate rights account certificates (RACs):<ol>
<li>Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> to create a client session.</li>
<li>Set the <i>uIndex</i> parameter to zero and the  <i>uFlags</i> parameter to <b>DRM_EL_GROUPIDENTITY</b> and call <b>DRMEnumerateLicense</b>.</li>
<li>Examine the RAC returned. If it is not the one sought, increment <i>uIndex</i> and call <b>DRMEnumerateLicense</b> again. You can continue iterating until you find the correct RAC or the function returns  <b>E_DRM_NO_MORE_DATA</b>.</li>
</ol>


Perform the following steps to enumerate client licensor certificates (CLCs):<ol>
<li>Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> to create a client session.</li>
<li>Set the <i>uIndex</i> parameter to zero and the  <i>uFlags</i> parameter to <b>DRM_EL_CLIENTLICENSOR</b> and call <b>DRMEnumerateLicense</b>.</li>
<li>Examine the CLC returned. If it is not the one sought, increment <i>uIndex</i> and call <b>DRMEnumerateLicense</b> again. You can continue iterating until you find the correct CLC or the function returns  <b>E_DRM_NO_MORE_DATA</b>.</li>
</ol>


Perform the following steps to enumerate issuance license templates:<ol>
<li>Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> to create a client session.</li>
<li>Set the <i>uIndex</i> parameter to zero and the  <i>uFlags</i> parameter to <b>DRM_EL_ISSUANCELICENSE_TEMPLATE</b> and call <b>DRMEnumerateLicense</b>.</li>
<li>Examine the template. If it is not the one sought, increment <i>uIndex</i> and call <b>DRMEnumerateLicense</b> again. You can continue iterating until you find the correct template or the function returns  <b>E_DRM_NO_MORE_DATA</b>.</li>
</ol>


Perform the following steps to enumerate revocation lists:<ol>
<li>Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> or <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreatelicensestoragesession">DRMCreateLicenseStorageSession</a> to create a session object. Use the client session handle to retrieve revocation lists for rights account or client licensor certificates. Use the license storage session handle to retrieve the revocation lists for end user licenses.</li>
<li>Set the <i>uIndex</i> parameter to zero and the  <i>uFlags</i> parameter to <b>DRM_EL_REVOCATIONLIST</b> and call <b>DRMEnumerateLicense</b>.</li>
<li>If the revocation list is not the one sought, increment <i>uIndex</i> and call <b>DRMEnumerateLicense</b> again. You can continue iterating until you find the correct list or the function returns  <b>E_DRM_NO_MORE_DATA</b>.</li>
</ol>


You must call <b>DRMEnumerateLicense</b> twice to retrieve one license. Set the <i>wszCertificateData</i> to <b>NULL</b> on the first call to retrieve the required buffer size. Allocate memory and call <b>DRMEnumerateLicense</b> again. This is illustrated by the following example.


```cpp
// Call DRMEnumerateLicense with the wszCertificateData parameter set
// to NULL.
hr = DRMEnumerateLicense( 
         hClient,                          // Client session handle
         DRM_EL_SPECIFIED_CLIENTLICENSOR,  // Flags
         0,                                // Index
         &fShared,                         // Shared license
         &uiClientLicensorCertLength,      // Certificate length
         NULL                              // Certificate
         );

if ( FAILED( hr ) && ( E_DRM_NO_MORE_DATA != hr ) )
{
   goto e_Exit;
}

// There are no client licensor certificates. Acquire one.
else if ( E_DRM_NO_MORE_DATA == hr )
{
    // TODO: Acquire a client licensor certificate.
}

// A client licensor certificate was found. Allocate memory and
// call DRMEnumerateLicense again.
else
{

   wszClientLicensorCert = new WCHAR[ uiClientLicensorCertLength ];
   if ( NULL == wszClientLicensorCert )
   {
      hr = E_OUTOFMEMORY;
      goto e_Exit;
   }

   hr = DRMEnumerateLicense( 
         hClient,                          // Client session handle
         DRM_EL_SPECIFIED_CLIENTLICENSOR,  // Flags
         0,                                // Index
         &fShared,                         // Shared license
         &uiClientLicensorCertLength,      // Certificate length
         wszClientLicensorCert             // Certificate
         );

   if ( FAILED( hr ) )
   {
      goto e_Exit;
   }
}

e_Exit:

    if ( NULL != hClient )
    {
        hr = DRMCloseSession( hClient );
    }

    if ( NULL != wszUserId )
    {
        delete [] wszUserId;
    }


    if ( NULL != wszLicensingSvr )
    {
        delete [] wszLicensingSvr;
    }

    if ( NULL != wszClientLicensorCert )
    {
        delete [] wszClientLicensorCert;
    }

    return hr;


```

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/offlinesigning-getcertificate-cpp">OfflineSigning_GetCertificate.cpp</a>
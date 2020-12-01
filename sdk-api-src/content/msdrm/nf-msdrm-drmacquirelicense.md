---
UID: NF:msdrm.DRMAcquireLicense
title: DRMAcquireLicense function (msdrm.h)
description: Attempts to acquire an end-user license or client licensor certificate asynchronously.
helpviewer_keywords: ["DRMAcquireLicense","DRMAcquireLicense function [Active Directory Rights Management Services SDK 1.0]","DRM_AL_CANCEL","DRM_AL_FETCHNOADVISORY","DRM_AL_NONSILENT","DRM_AL_NOPERSIST","DRM_AL_NOUI","msdrm/DRMAcquireLicense","rm.drmacquirelicense"]
old-location: rm\drmacquirelicense.htm
tech.root: rm
ms.assetid: 0d4ce794-8384-4f1c-bc8c-1e67fbb5f987
ms.date: 12/05/2018
ms.keywords: DRMAcquireLicense, DRMAcquireLicense function [Active Directory Rights Management Services SDK 1.0], DRM_AL_CANCEL, DRM_AL_FETCHNOADVISORY, DRM_AL_NONSILENT, DRM_AL_NOPERSIST, DRM_AL_NOUI, msdrm/DRMAcquireLicense, rm.drmacquirelicense
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
 - DRMAcquireLicense
 - msdrm/DRMAcquireLicense
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
 - DRMAcquireLicense
---

# DRMAcquireLicense function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available 
    for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, 
    Windows 7, Windows Server 2012, and Windows 8. It may be altered or 
    unavailable in subsequent versions. Instead, use 
    <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 
    which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMAcquireLicense</b> function attempts to acquire an end-user license or client licensor certificate asynchronously.

## -parameters

### -param hSession [in]

A handle to a client or license storage session.

A client session handle is obtained by using the 
       <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> function. In this case, 
       a client licensor certificate is acquired. The application callback function specified in the <b>DRMCreateClientSession</b> function will be called with the <a href="/previous-versions/windows/desktop/adrms_sdk/drm-msg-acquire-clientlicensor">DRM_MSG_ACQUIRE_CLIENTLICENSOR</a> message to provide status feedback.

A license storage session handle is obtained by calling the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreatelicensestoragesession">DRMCreateLicenseStorageSession</a> function. In this case, an end-user license is acquired. The application callback function specified in the client session passed in the <i>hClient</i> parameter of the  <b>DRMCreateLicenseStorageSession</b> function will be called with the <a href="/previous-versions/windows/desktop/adrms_sdk/drm-msg-acquire-license">DRM_MSG_ACQUIRE_LICENSE</a> message to provide status feedback.

### -param uFlags [in]

Specifies options for the function call. This parameter can be zero or a combination of one or more of the following flags.



#### DRM_AL_NONSILENT ()

Nonsilent license acquisition is not supported. <b>DRMAcquireLicense</b> returns <b>E_INVALIDARG</b> if this flag is set.

For Rights Management Services (RMS) client 1.0, acquire the license nonsilently. The default is silent license acquisition.



#### DRM_AL_NOPERSIST ()

Store the license only in the temporary (in-memory) license store. The default is to store the license in the permanent license store.



#### DRM_AL_CANCEL ()

Cancel the previous request.



#### DRM_AL_FETCHNOADVISORY ()

Do not acquire revocation lists required by the license. The default action is to acquire all revocation lists that a returned license requires. All revocation lists must still be registered, however, by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmregisterrevocationlist">DRMRegisterRevocationList</a> function.



#### DRM_AL_NOUI ()

This flag suppresses the Windows network authentication dialog box. If the license request is denied because the user does not have permission, this flag will prevent the network authentication dialog box from being displayed. This is useful when attempting to handle license acquisition on a background or other non-user interface thread because you can avoid potentially confusing dialog boxes. If authentication does fail, and this flag is specified, the callback that is associated with the request will immediately receive an error of <b>E_DRM_LICENSEACQUISITIONFAILED</b>.

If <i>hSession</i> is a client session handle, this flag is ignored.

### -param wszGroupIdentityCredential [in]

An optional <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificate</a> (RAC). If this is not used, this function will check the license store for a RAC that matches the license used to create <i>hSession</i>. If none is found, this function will fail.

### -param wszRequestedRights [in]

This parameter is reserved and must be <b>NULL</b>.

### -param wszCustomData [in]

Optional application-specific data that might be required for a license. This must be a valid XML string. After returning control to the caller, this function creates a license request by using the application-specific data specified here.

### -param wszURL [in]

A license acquisition URL. This parameter is required when a client licensor certificate is being acquired and optional when an end-user license is being acquired. The URL can be used for both silent and nonsilent license acquisition. When present, this URL overrides the URL specified in the license that was used to create the license storage session passed into <i>hSession</i>.

A license may hold multiple license acquisition URLs, but only the first is used by default. To use any of the other URLs specified, you must parse the license. For more information, see the Remarks section.

### -param pvContext [in]

A 32-bit, application-defined value that is sent in the <i>pvContext</i> parameter of the callback function. This value can be a pointer to data, a pointer to an event handle, or whatever else the custom callback function is designed to handle. For more information, see <a href="/previous-versions/windows/desktop/api/msdrmdefs/nc-msdrmdefs-drmcallback">Callback Prototype</a>.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

This function is used for retrieving an end-user license or client licensor certificate asynchronously. There 
     is no synchronous version of this function. To cancel a license request in process, call 
     <b>DRMAcquireLicense</b> again with 
     <b>DRM_AL_CANCEL</b> specified in <i>uFlags</i>. The progress of this 
     function, and any data returned,  will be returned to the callback function (see 
     <a href="/previous-versions/windows/desktop/adrms_sdk/creating-a-callback-function">Creating a Callback Function</a>).

If the retrieved end-user license requires any revocation lists, these are acquired at the same time, unless 
     <b>DRM_AL_FETCHNOADVISORY</b> is specified in <i>uFlags</i>. A failure to 
     retrieve required revocation lists will be indicated by <b>E_DRM_NO_CONNECT</b>. The 
     application must register any retrieved lists by using 
     <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmregisterrevocationlist">DRMRegisterRevocationList</a>.

This function can occur silently or nonsilently.

<div class="alert"><b>Note</b>  Nonsilent license acquisition is supported only in RMS client 1.0. Effective with RMS client 1.0 SP1, 
     nonsilent license acquisition is no longer supported, and MSDRMCtrl.dll is not shipped.</div>
<div> </div>
In nonsilent license acquisition, a license acquisition URL is returned to the callback function in a 
     <a href="/windows/desktop/api/msdrmdefs/ns-msdrmdefs-drm_license_acq_data">DRM_LICENSE_ACQ_DATA</a> structure. The application then 
     opens a web browser that is directed to a URL that specifies an HTML page that contains the ActiveX control in 
     MSDRMCtrl.dll. The page is used to obtain additional information, such as a credit card number, and 
     then calls the ActiveX control's <b>AcquireLicense</b> 
     function, which causes license acquisition to proceed as normal. The license can only be returned to the 
     permanent license store.

In  silent license acquisition, no webpages need be opened, and license acquisition progress is noted in the 
     application's callback function.

The retrieved license is added to the temporary or permanent license store, depending on whether 
     <b>DRM_AL_NOPERSIST</b> is specified or not. In nonsilent license acquisition, the acquired 
     license cannot be added to the temporary license store, only to the permanent license store, where it must be 
     retrieved by  using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a>. The 
     following list describes possible combinations of license acquisition type with license store type.

<table>
<tr>
<th>License store</th>
<th>Silent acquisition</th>
<th>Nonsilent acquisition</th>
</tr>
<tr>
<td>Temporary</td>
<td><b>DRM_AL_NOPERSIST</b></td>
<td>Not possible</td>
</tr>
<tr>
<td>Permanent</td>
<td>No flags</td>
<td><b>DRM_AL_NONSILENT</b></td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Although the issuance license is signed and protected by encryption, it would be possible for a malicious publisher to include the URL of a malicious website; there is no way to verify the nature of this URL in advance.</div>
<div> </div>
AD RMS allows an administrator to specify an extranet licensing  URL in addition to an internal (intranet) URL. Each  URL is copied into the license under a separate &lt;DISTRIBUTIONPOINT&gt; node with the internal URL appearing first. This is illustrated by the following example.


```xml

      <DISTRIBUTIONPOINT>
      - <OBJECT type="License-Acquisition-URL">
          <ID type="MS-GUID">
            {0F45FD50-383B-43EE-90A4-ED013CD0CFE5}
          </ID> 
          <NAME>DRM Server Cluster</NAME> 
          <ADDRESS type="URL">
            https://corprights/_wmcs/licensing
          </ADDRESS> 
        </OBJECT>
      </DISTRIBUTIONPOINT>
      <DISTRIBUTIONPOINT>
      - <OBJECT type="Extranet-License-Acquisition-URL">
          <ID type="MS-GUID">
            {94BF969A-CA04-44d6-AA96-51071281FAG2}
          </ID> 
          <NAME>DRM Server Cluster</NAME> 
          <ADDRESS type="URL">
            https://corprights.example.com/_wmcs/licensing
          </ADDRESS> 
        </OBJECT>
      </DISTRIBUTIONPOINT>

```


Multiple URLs are often specified so that  users can access protected content both at work and at home. The second URL provides a license acquisition point that does not require the user working at home to log on to the corporate network. The <b>DRMAcquireLicense</b> function, however, uses the first URL by default. Therefore, to allow the consumer to use an alternate URL, your application must parse the license.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>
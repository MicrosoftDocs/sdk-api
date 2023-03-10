---
UID: NF:msdrm.DRMAcquireIssuanceLicenseTemplate
title: DRMAcquireIssuanceLicenseTemplate function (msdrm.h)
description: Asynchronously retrieves issuance license templates from a server.
helpviewer_keywords: ["DRMAcquireIssuanceLicenseTemplate","DRMAcquireIssuanceLicenseTemplate function [Active Directory Rights Management Services SDK 1.0]","DRM_AILT_CANCEL","DRM_AILT_NONSILENT","DRM_AILT_OBTAIN_ALL","msdrm/DRMAcquireIssuanceLicenseTemplate","rm.drmacquireissuancelicensetemplate"]
old-location: rm\drmacquireissuancelicensetemplate.htm
tech.root: rm
ms.assetid: 15f6d38a-d4f2-4af4-8bbc-bc44ac14db0c
ms.date: 12/05/2018
ms.keywords: DRMAcquireIssuanceLicenseTemplate, DRMAcquireIssuanceLicenseTemplate function [Active Directory Rights Management Services SDK 1.0], DRM_AILT_CANCEL, DRM_AILT_NONSILENT, DRM_AILT_OBTAIN_ALL, msdrm/DRMAcquireIssuanceLicenseTemplate, rm.drmacquireissuancelicensetemplate
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
req.target-min-winversvr: Windows Server 2008
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
ms.custom: 19H1
f1_keywords:
 - DRMAcquireIssuanceLicenseTemplate
 - msdrm/DRMAcquireIssuanceLicenseTemplate
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
 - DRMAcquireIssuanceLicenseTemplate
---

# DRMAcquireIssuanceLicenseTemplate function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMAcquireIssuanceLicenseTemplate</b> function asynchronously retrieves issuance license templates from a server.

## -parameters

### -param hClient [in]

A handle to a client session. The handle is obtained by calling the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> function. When you call  <b>DRMCreateClientSession</b>, you must specify a callback function that AD RMS can use to return the result of an operation. A string that contains the templates  is sent to the callback function in a <a href="/previous-versions/windows/desktop/adrms_sdk/drm-msg-acquire-issuance-license-template">DRM_MSG_ACQUIRE_ISSUANCE_LICENSE_TEMPLATE</a> message.

### -param uFlags [in]

Specifies options for the function call. This parameter can be a combination of one or more of the following flags.



#### DRM_AILT_NONSILENT ()

nonsilent template acquisition is supported. That is, an authentication prompt is displayed if an access control list (ACL) is applied to the template and default authentication fails.



#### DRM_AILT_OBTAIN_ALL ()

Retrieves all templates from the server and adds them to the local store:


<ul>
<li>Templates in the local store that are not present on the server are deleted from the local store.</li>
<li>Templates in the local store that have been updated on the server are replaced.</li>
<li>Templates that are found on the server but not in the local store are added to the local store.</li>
</ul>




#### DRM_AILT_CANCEL ()

Cancels the previous request.

### -param pvReserved [in]

Reserved for future use. This parameter must be <b>NULL</b>.

### -param cTemplates [in]

Reserved for future use. This value must be zero.

### -param pwszTemplateIds [in, optional]

Reserved for future use. This parameter must be <b>NULL</b>.

### -param wszUrl [in]

A null-terminated Unicode string that contains the template acquisition URL. You can retrieve this value by calling <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetservicelocation">DRMGetServiceLocation</a> and setting the <i>uServiceType</i> parameter to <b>DRM_SERVICE_TYPE_CLIENTLICENSOR</b>.

### -param pvContext [in]

A 32-bit, application-defined value that is returned in the <i>pvContext</i> parameter of the callback function. This value can be a pointer to data, a pointer to an event handle, or whatever else the custom callback function is designed to handle. For more information, see <a href="/previous-versions/windows/desktop/api/msdrmdefs/nc-msdrmdefs-drmcallback">Callback Prototype</a>.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <b>DRMAcquireIssuanceLicenseTemplate</b> function is asynchronous. It returns immediately with a value of S_OK or an error code. To cancel a request in process, 
 call the function  with <b>DRM_AILT_CANCEL</b> specified for the <i>uFlags</i> parameter. To determine the result of the template retrieval operation, you must examine the <i>hr</i> parameter in the <a href="/previous-versions/windows/desktop/adrms_sdk/drm-msg-acquire-issuance-license-template">DRM_MSG_ACQUIRE_ISSUANCE_LICENSE_TEMPLATE</a> message that AD RMS sends to your callback function.

The template collection is saved in the template store of the local AD RMS store. Each template is stored in a file with the format TMP-<i>HashValue</i>-<i>TemplateGUID</i> where the hash value is a base64-encoded SHA-1 hash of server public key. You can call the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a> function to enumerate the templates.

If properly configured, AD RMS clients can automatically obtain templates from the AD RMS server by using a WMI job in the task scheduler. Therefore, if WMI distribution is enabled, call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a> to enumerate the rights policy templates from the local template store. Applications should avoid calling <b>DRMAcquireIssuanceLicenseTemplate</b> because the WMI job automatically copies templates to the client computer. However, <b>DRMAcquireIssuanceLicenseTemplate</b> can be used to retrieve templates from multiple servers, functionality not supported by the WMI job. You can also use it to retrieve templates if your application relies on a server lockbox. The WMI job is only available to applications that use a client lockbox.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmacquirelicense">DRMAcquireLicense</a>
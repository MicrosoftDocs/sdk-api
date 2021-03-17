---
UID: NF:msdrm.DRMCreateClientSession
title: DRMCreateClientSession function (msdrm.h)
description: Creates a client session, which hosts license storage sessions and is used in activation and other function calls.
helpviewer_keywords: ["DRMCreateClientSession","DRMCreateClientSession function [Active Directory Rights Management Services SDK 1.0]","DRM_DEFAULTGROUPIDTYPE_PASSPORT","DRM_DEFAULTGROUPIDTYPE_WINDOWSAUTH","msdrm/DRMCreateClientSession","rm.drmcreateclientsession"]
old-location: rm\drmcreateclientsession.htm
tech.root: rm
ms.assetid: 4b8928a0-1d72-47ee-a357-47fb5777d60c
ms.date: 12/05/2018
ms.keywords: DRMCreateClientSession, DRMCreateClientSession function [Active Directory Rights Management Services SDK 1.0], DRM_DEFAULTGROUPIDTYPE_PASSPORT, DRM_DEFAULTGROUPIDTYPE_WINDOWSAUTH, msdrm/DRMCreateClientSession, rm.drmcreateclientsession
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
 - DRMCreateClientSession
 - msdrm/DRMCreateClientSession
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
 - DRMCreateClientSession
---

# DRMCreateClientSession function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateClientSession</b> function creates a client session, which hosts license storage sessions and is used in activation and other function calls.

## -parameters

### -param pfnCallback [in]

A pointer to an application-defined callback function that will receive asynchronous function status messages in response to other AD RMS functions, such as <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmactivate">DRMActivate</a>. The format of this callback function is defined in <a href="/previous-versions/windows/desktop/api/msdrmdefs/nc-msdrmdefs-drmcallback">Callback Prototype</a>. This parameter cannot be <b>NULL</b>.

### -param uCallbackVersion [in]

Specifies the version of the callback function. Currently, only version zero is supported.

### -param wszGroupIDProviderType [in]

A pointer to a null-terminated Unicode string that specifies the authentication type of the submitted <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificate</a> (RAC). This can be one of the following values.



#### DRM_DEFAULTGROUPIDTYPE_WINDOWSAUTH

Use Windows authentication. Specify this value also for an Active Directory Federation Services (ADFS) RAC.



#### DRM_DEFAULTGROUPIDTYPE_PASSPORT

Use Passport authentication.

### -param wszGroupID [in, optional]

A pointer to a null-terminated Unicode string that contains an email address for the user in the format <i>someone@example.com</i>. Typically, this value already exists in Active Directory (AD) and is the same ID as that supplied in the logon credentials. If it is not the same, later calls to <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmisactivated">DRMIsActivated</a> and <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a> will fail. For more information, see Remarks.

Set this parameter to  <b>NULL</b> if you intend only to use the client session handle created by this function to retrieve a service location by calling <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetservicelocation">DRMGetServiceLocation</a>.

### -param phClient [out]

A pointer to a <b>DRMHSESSION</b> value that receives the client session handle. When you have finished using the client session, close it by passing this handle to the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosesession">DRMCloseSession</a> function.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

If this function is successful, the AD RMS server returns a client session handle that is used by <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmactivate">DRMActivate</a> to create a rights account certificate (RAC) in the license store for the new client session. The RAC is created by using the credentials of the logged–on user. If the email address specified in the <i>wszGroupID</i> parameter does not match that specified in the credentials, functions such as <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmisactivated">DRMIsActivated</a> and <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a> that use information associated with the client session to search the license store for the RAC will fail.

For example, assume that  the user logged on by using cat@example.com but the <i>wszGroupID</i> parameter is set to dog@example.com. The RAC is created for cat@example.com. The <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a> function, however, searches the license store for a RAC that contains  dog@example.com and fails.

All license storage sessions must be closed before closing the client session. When you have finished using the client session, close it by passing the handle provided by this function to the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosesession">DRMCloseSession</a> function.

The <b>DRMCreateClientSession</b> function cannot be called concurrently by different processes running as different users on the same computer if one or more of these processes is a service process. A call by a second  process, for example, can succeed only after the client session handle for the first process has been closed.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/creating-a-callback-function">Creating a Callback Function</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosesession">DRMCloseSession</a>
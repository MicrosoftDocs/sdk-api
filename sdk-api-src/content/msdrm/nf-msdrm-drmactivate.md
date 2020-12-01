---
UID: NF:msdrm.DRMActivate
title: DRMActivate function (msdrm.h)
description: Obtains a lockbox and machine certificate for a machine or a rights account certificate for a user.
helpviewer_keywords: ["DRMActivate","DRMActivate function [Active Directory Rights Management Services SDK 1.0]","DRM_ACTIVATE_CANCEL","DRM_ACTIVATE_DELAYED","DRM_ACTIVATE_GROUPIDENTITY","DRM_ACTIVATE_MACHINE","DRM_ACTIVATE_SHARED_GROUPIDENTITY","DRM_ACTIVATE_SILENT","DRM_ACTIVATE_TEMPORARY","msdrm/DRMActivate","rm.drmactivate"]
old-location: rm\drmactivate.htm
tech.root: rm
ms.assetid: d3f4ac2c-95d9-4273-a679-81670dd62d28
ms.date: 12/05/2018
ms.keywords: DRMActivate, DRMActivate function [Active Directory Rights Management Services SDK 1.0], DRM_ACTIVATE_CANCEL, DRM_ACTIVATE_DELAYED, DRM_ACTIVATE_GROUPIDENTITY, DRM_ACTIVATE_MACHINE, DRM_ACTIVATE_SHARED_GROUPIDENTITY, DRM_ACTIVATE_SILENT, DRM_ACTIVATE_TEMPORARY, msdrm/DRMActivate, rm.drmactivate
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
req.product: Rights Management Services client v1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - DRMActivate
 - msdrm/DRMActivate
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
 - DRMActivate
---

# DRMActivate function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMActivate</b> function obtains a lockbox and <a href="/previous-versions/windows/desktop/adrms_sdk/m-gly">machine certificate</a> for a machine or a <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificate</a> for a user.

## -parameters

### -param hClient [in]

A handle to a client session, created by <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a>.

### -param uFlags [in]

Specifies the type of activation wanted, plus additional options; for more information, see Remarks. This parameter can be a combination of one or more of the following flags.



#### DRM_ACTIVATE_MACHINE

Activate the computer. The <b>DRM_ACTIVATE_SILENT</b> flag is also required, but the <b>DRM_ACTIVATE_GROUPIDENTITY</b> flag must not be set. The <i>pActServInfo</i> parameter is ignored.

Each computer is activated on a per-user basis. That is, the machine certificate is generated and stored for the currently logged-in user.

The application callback function specified in the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> function will be called with the <a href="/previous-versions/windows/desktop/adrms_sdk/drm-msg-activate-machine">DRM_MSG_ACTIVATE_MACHINE</a> message to provide machine activation status feedback.



#### DRM_ACTIVATE_GROUPIDENTITY

Activates a rights account. This flag cannot be combined with <b>DRM_ACTIVATE_MACHINE</b>.

The <b>DRM_ACTIVATE_SILENT</b> flag is required for RMS v1.0  SP2 and Windows Vista. The <b>DRM_ACTIVATE_SILENT</b> flag is, however, optional for Windows Vista with SP1 and Windows Server 2008.

The application callback function specified in the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> function will be called with the <a href="/previous-versions/windows/desktop/adrms_sdk/drm-msg-activate-groupidentity">DRM_MSG_ACTIVATE_GROUPIDENTITY</a> message to provide rights account activation status feedback.



#### DRM_ACTIVATE_TEMPORARY

Acquire a temporary <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificate</a> (RAC). A temporary RAC is only good for a short period of time, but it is stored in the permanent license store. This flag is ignored in nonsilent activation; for more information,  see Remarks.



#### DRM_ACTIVATE_CANCEL

Cancel an in-progress activation attempt.



#### DRM_ACTIVATE_SILENT

Activate a user without displaying a Windows password dialog box. This flag is required for <b>DRM_ACTIVATE_MACHINE</b> and optional for <b>DRM_ACTIVATE_GROUPIDENTITY</b>, depending on the operating system. For more information, see the <b>DRM_ACTIVATE_GROUPIDENTITY</b> parameter.

If this flag is used with <b>DRM_ACTIVATE_GROUPIDENTITY</b>, the <i>pActServInfo</i> parameter cannot be <b>NULL</b>. If it is used with <b>DRM_ACTIVATE_MACHINE</b>, <i>pActServInfo</i> is ignored.



#### DRM_ACTIVATE_SHARED_GROUPIDENTITY

This flag is not used.



#### DRM_ACTIVATE_DELAYED

Delayed machine activation. In normal silent activation, the client receives a CAB file that contains activation files that are expanded and run automatically. With this flag, the files are saved to a location that is passed to the <i>pvParam</i> parameter of the callback function, where a client can check them for viruses before expanding and running them.

### -param uLangID [in]

The language ID used by the application. If this parameter is set to zero, the default language ID for the logged-on user is used.

### -param pActServInfo [in]

Optional server information. If the client has not been configured to use Active Directory Federation Services (ADFS) with AD RMS, you can pass <b>NULL</b> to use the Windows Live ID service for service discovery. If the client has been configured to use ADFS, you must pass the Windows Live certification URL. <!-- Currently, the Windows Live ID certification service URL is https://certification.isv.drm.microsoft.com/certification/certification.asmx.--> For more information about service discovery, see  <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetservicelocation">DRMGetServiceLocation</a>.

### -param pvContext [in]

A 32-bit, application-defined value that is sent in the <i>pvContext</i> parameter of the callback function. This value can be a pointer to data, a pointer to an event handle, or whatever else the custom callback function is designed to handle. For more information, see <a href="/previous-versions/windows/desktop/api/msdrmdefs/nc-msdrmdefs-drmcallback">Callback Prototype</a>.

### -param hParentWnd [in]

Parent window handle used in nonsilent Windows Live ID activation (user activation only). In nonsilent activation, a Windows Live ID window opens to request user information. This parameter allows the application to assign an arbitrary window as the window's parent. If this parameter is <b>NULL</b>, the active window is used.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

If an application attempts to activate a user on a computer that has not yet been activated, the function will fail. We recommend that an application call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmisactivated">DRMIsActivated</a> before calling this function to determine the activation status of the computer. Activating a machine that is already activated will overwrite the existing lockbox and machine certificate. Activating a user a second time will add an additional <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificate</a> to the computer. A user needs to activate a particular computer only once, although updates in the lockbox architecture may require downloading and activating a new lockbox.

There are several options in activation.<table>
<tr>
<th>Option</th>
<th>Description</th>
</tr>
<tr>
<td>Silent or nonsilent</td>
<td>Nonsilent activation is the default. Silent activation is specified by <b>DRM_ACTIVATE_SILENT</b> and is required for machine activation.  If silent activation is specified and <i>pActServInfo</i> is not <b>NULL</b>, the function creates and sends an activation request to the URL specified in the <b>wszURL</b> member of <i>pActServInfo</i>. For more information, see <a href="/windows/desktop/api/msdrmdefs/ns-msdrmdefs-drm_actserv_info">DRM_ACTSERV_INFO</a>.</td>
</tr>
<tr>
<td>Windows or Windows Live ID</td>
<td>This is determined by the type of client handle passed in to <i>hClient</i>.</td>
</tr>
<tr>
<td>Temporary or permanent</td>
<td>This applies only to a <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificate</a> (RAC), not to a machine certificate. Permanent activation is the default. Temporary is specified by the <b>DRM_ACTIVATE_TEMPORARY</b> flag. When you acquire a temporary RAC by using the <b>DRM_ACTIVATE_TEMPORARY</b> flag, the RAC is stored in the permanent license store, though it will expire shortly. The default validity time for a temporary RAC is 15 minutes, although this can be changed by the AD RMS service's administrator. To avoid cluttering the license store with expired RACs, you should delete a temporary RAC when ending a client session.</td>
</tr>
</table>
 



The following list describes what happens with combinations of these options.<table>
<tr>
<th>Option</th>
<th>Temporary</th>
<th>Permanent</th>
</tr>
<tr>
<td>Silent Windows</td>
<td>Activation occurs without a dialog box. The user currently logged in is activated.</td>
<td>Activation occurs without a dialog box. The user currently logged in is activated.</td>
</tr>
<tr>
<td>Nonsilent Windows</td>
<td>A Windows password dialog box appears. The user specified is activated.</td>
<td>A Windows password dialog box appears. The user specified is activated.</td>
</tr>
<tr>
<td>Silent Windows Live ID</td>
<td>Not allowed.</td>
<td>Not allowed.</td>
</tr>
<tr>
<td>Nonsilent Windows Live ID</td>
<td>A Windows Live ID login window appears. The user specified is activated.</td>
<td>A Windows Live ID login window appears. The user specified is activated.</td>
</tr>
</table>
 



During execution, <b>DRMActivate</b> calls into the user-defined callback function and sets the <i>msg</i> parameter to <b>DRM_MSG_ACTIVATE_MACHINE</b> or <b>DRM_MSG_ACTIVATE_GROUPIDENTITY</b>. For more information, see <a href="/previous-versions/windows/desktop/adrms_sdk/creating-a-callback-function">Creating a Callback Function</a>.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/activating-a-computer">Activating a Computer</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/activating-a-user">Activating a User</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/creating-a-callback-function">Creating a Callback Function</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmisactivated">DRMIsActivated</a>
---
UID: NF:msdrm.DRMActivate
title: DRMActivate function
author: windows-sdk-content
description: Obtains a lockbox and machine certificate for a machine or a rights account certificate for a user.
old-location: rm\drmactivate.htm
tech.root: AdRms_Sdk
ms.assetid: d3f4ac2c-95d9-4273-a679-81670dd62d28
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DRMActivate, DRMActivate function [Active Directory Rights Management Services SDK 1.0], DRM_ACTIVATE_CANCEL, DRM_ACTIVATE_DELAYED, DRM_ACTIVATE_GROUPIDENTITY, DRM_ACTIVATE_MACHINE, DRM_ACTIVATE_SHARED_GROUPIDENTITY, DRM_ACTIVATE_SILENT, DRM_ACTIVATE_TEMPORARY, msdrm/DRMActivate, rm.drmactivate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMActivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client v1.0 SP2 or later
---

# DRMActivate function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMActivate</b> function obtains a lockbox and <a href="https://msdn.microsoft.com/en-us/library/Aa362706(v=VS.85).aspx">machine certificate</a> for a machine or a <a href="https://msdn.microsoft.com/en-us/library/Aa362726(v=VS.85).aspx">rights account certificate</a> for a user. 


## -parameters




### -param hClient [in]

A handle to a client session, created by <a href="https://msdn.microsoft.com/4b8928a0-1d72-47ee-a357-47fb5777d60c">DRMCreateClientSession</a>.


### -param uFlags [in]

Specifies the type of activation wanted, plus additional options; for more information, see Remarks. This parameter can be a combination of one or more of the following flags.



#### DRM_ACTIVATE_MACHINE

Activate the computer. The <b>DRM_ACTIVATE_SILENT</b> flag is also required, but the <b>DRM_ACTIVATE_GROUPIDENTITY</b> flag must not be set. The <i>pActServInfo</i> parameter is ignored.

Each computer is activated on a per-user basis. That is, the machine certificate is generated and stored for the currently logged-in user.

The application callback function specified in the <a href="https://msdn.microsoft.com/4b8928a0-1d72-47ee-a357-47fb5777d60c">DRMCreateClientSession</a> function will be called with the <a href="https://msdn.microsoft.com/1006464b-5fd2-4bc0-ac43-aacc5cd02322">DRM_MSG_ACTIVATE_MACHINE</a> message to provide machine activation status feedback.



#### DRM_ACTIVATE_GROUPIDENTITY

Activates a rights account. This flag cannot be combined with <b>DRM_ACTIVATE_MACHINE</b>.

The <b>DRM_ACTIVATE_SILENT</b> flag is required for RMS v1.0  SP2 and Windows Vista. The <b>DRM_ACTIVATE_SILENT</b> flag is, however, optional for Windows Vista with SP1 and Windows Server 2008.

The application callback function specified in the <a href="https://msdn.microsoft.com/4b8928a0-1d72-47ee-a357-47fb5777d60c">DRMCreateClientSession</a> function will be called with the <a href="https://msdn.microsoft.com/49c8606a-c2d9-4380-9b99-139d75b0689b">DRM_MSG_ACTIVATE_GROUPIDENTITY</a> message to provide rights account activation status feedback.



#### DRM_ACTIVATE_TEMPORARY

Acquire a temporary <a href="https://msdn.microsoft.com/en-us/library/Aa362726(v=VS.85).aspx">rights account certificate</a> (RAC). A temporary RAC is only good for a short period of time, but it is stored in the permanent license store. This flag is ignored in nonsilent activation; for more information,  see Remarks.



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

Optional server information. If the client has not been configured to use Active Directory Federation Services (ADFS) with AD RMS, you can pass <b>NULL</b> to use the Windows Live ID service for service discovery. If the client has been configured to use ADFS, you must pass the Windows Live certification URL. Currently, the Windows Live ID certification service URL is https://certification.drm.microsoft.com/certification. For more information about service discovery, see  <a href="https://msdn.microsoft.com/f7cbc3ba-009f-4a35-999e-139d41961fd9">DRMGetServiceLocation</a>.


### -param pvContext [in]

A 32-bit, application-defined value that is sent in the <i>pvContext</i> parameter of the callback function. This value can be a pointer to data, a pointer to an event handle, or whatever else the custom callback function is designed to handle. For more information, see <a href="https://msdn.microsoft.com/41c200df-afbc-43a5-8046-d131fec3261a">Callback Prototype</a>.


### -param hParentWnd [in]

Parent window handle used in nonsilent Windows Live ID activation (user activation only). In nonsilent activation, a Windows Live ID window opens to request user information. This parameter allows the application to assign an arbitrary window as the window's parent. If this parameter is <b>NULL</b>, the active window is used.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



If an application attempts to activate a user on a computer that has not yet been activated, the function will fail. We recommend that an application call <a href="https://msdn.microsoft.com/f6c7bc7f-e9e8-4fc4-b30f-31bc0f5f46aa">DRMIsActivated</a> before calling this function to determine the activation status of the computer. Activating a machine that is already activated will overwrite the existing lockbox and machine certificate. Activating a user a second time will add an additional <a href="https://msdn.microsoft.com/en-us/library/Aa362726(v=VS.85).aspx">rights account certificate</a> to the computer. A user needs to activate a particular computer only once, although updates in the lockbox architecture may require downloading and activating a new lockbox.

There are several options in activation.<table>
<tr>
<th>Option</th>
<th>Description</th>
</tr>
<tr>
<td>Silent or nonsilent</td>
<td>Nonsilent activation is the default. Silent activation is specified by <b>DRM_ACTIVATE_SILENT</b> and is required for machine activation.  If silent activation is specified and <i>pActServInfo</i> is not <b>NULL</b>, the function creates and sends an activation request to the URL specified in the <b>wszURL</b> member of <i>pActServInfo</i>. For more information, see <a href="https://msdn.microsoft.com/2ea83a08-ab86-4635-8684-519808430ce9">DRM_ACTSERV_INFO</a>.</td>
</tr>
<tr>
<td>Windows or Windows Live ID</td>
<td>This is determined by the type of client handle passed in to <i>hClient</i>.</td>
</tr>
<tr>
<td>Temporary or permanent</td>
<td>This applies only to a <a href="https://msdn.microsoft.com/en-us/library/Aa362726(v=VS.85).aspx">rights account certificate</a> (RAC), not to a machine certificate. Permanent activation is the default. Temporary is specified by the <b>DRM_ACTIVATE_TEMPORARY</b> flag. When you acquire a temporary RAC by using the <b>DRM_ACTIVATE_TEMPORARY</b> flag, the RAC is stored in the permanent license store, though it will expire shortly. The default validity time for a temporary RAC is 15 minutes, although this can be changed by the AD RMS service's administrator. To avoid cluttering the license store with expired RACs, you should delete a temporary RAC when ending a client session.</td>
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
 



During execution, <b>DRMActivate</b> calls into the user-defined callback function and sets the <i>msg</i> parameter to <b>DRM_MSG_ACTIVATE_MACHINE</b> or <b>DRM_MSG_ACTIVATE_GROUPIDENTITY</b>. For more information, see <a href="https://msdn.microsoft.com/7d880b74-1934-4282-a7ca-1dac3602d6b4">Creating a Callback Function</a>.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/f6980a9b-9e3c-47e4-b1c3-7e244ca77e44">Activating a Computer</a>



<a href="https://msdn.microsoft.com/c998647b-2e0c-4eee-bcf9-6c080340f5bb">Activating a User</a>



<a href="https://msdn.microsoft.com/7d880b74-1934-4282-a7ca-1dac3602d6b4">Creating a Callback Function</a>



<a href="https://msdn.microsoft.com/f6c7bc7f-e9e8-4fc4-b30f-31bc0f5f46aa">DRMIsActivated</a>
 

 


---
UID: NF:msdrm.DRMAcquireIssuanceLicenseTemplate
title: DRMAcquireIssuanceLicenseTemplate function
author: windows-sdk-content
description: Asynchronously retrieves issuance license templates from a server.
old-location: rm\drmacquireissuancelicensetemplate.htm
old-project: AdRms_Sdk
ms.assetid: 15f6d38a-d4f2-4af4-8bbc-bc44ac14db0c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DRMAcquireIssuanceLicenseTemplate, DRMAcquireIssuanceLicenseTemplate function [Active Directory Rights Management Services SDK 1.0], DRM_AILT_CANCEL, DRM_AILT_NONSILENT, DRM_AILT_OBTAIN_ALL, msdrm/DRMAcquireIssuanceLicenseTemplate, rm.drmacquireissuancelicensetemplate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: TF_SELECTIONSTYLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msdrm.dll
api_name:
-	DRMAcquireIssuanceLicenseTemplate
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMAcquireIssuanceLicenseTemplate function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMAcquireIssuanceLicenseTemplate</b> function asynchronously retrieves issuance license templates from a server.


## -parameters




### -param hClient [in]

A handle to a client session. The handle is obtained by calling the <a href="https://msdn.microsoft.com/4b8928a0-1d72-47ee-a357-47fb5777d60c">DRMCreateClientSession</a> function. When you call  <b>DRMCreateClientSession</b>, you must specify a callback function that AD RMS can use to return the result of an operation. A string that contains the templates  is sent to the callback function in a <a href="https://msdn.microsoft.com/e690fd96-c11f-43fe-85ad-466f62209e6d">DRM_MSG_ACQUIRE_ISSUANCE_LICENSE_TEMPLATE</a> message.


### -param uFlags [in]

Specifies options for the function call. This parameter can be a combination of one or more of the following flags.



#### DRM_AILT_NONSILENT ()

Non-silent template acquisition is supported. That is, an authentication prompt is displayed if an access control list (ACL) is applied to the template and default authentication fails.



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


### -param cTemplates

TBD


### -param pwszTemplateIds

TBD


### -param wszUrl

TBD


### -param pvContext [in]

A 32-bit, application-defined value that is returned in the <i>pvContext</i> parameter of the callback function. This value can be a pointer to data, a pointer to an event handle, or whatever else the custom callback function is designed to handle. For more information, see <a href="https://msdn.microsoft.com/41c200df-afbc-43a5-8046-d131fec3261a">Callback Prototype</a>.


#### - cReserved [in]

Reserved for future use. This value must be zero.


#### - pwszReserved [in, optional]

Reserved for future use. This parameter must be <b>NULL</b>.


#### - wszURL [in]

A null-terminated Unicode string that contains the template acquisition URL. You can retrieve this value by calling <a href="https://msdn.microsoft.com/f7cbc3ba-009f-4a35-999e-139d41961fd9">DRMGetServiceLocation</a> and setting the <i>uServiceType</i> parameter to <b>DRM_SERVICE_TYPE_CLIENTLICENSOR</b>.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <b>DRMAcquireIssuanceLicenseTemplate</b> function is asynchronous. It returns immediately with a value of S_OK or an error code. To cancel a request in process, 
 call the function  with <b>DRM_AILT_CANCEL</b> specified for the <i>uFlags</i> parameter. To determine the result of the template retrieval operation, you must examine the <i>hr</i> parameter in the <a href="https://msdn.microsoft.com/e690fd96-c11f-43fe-85ad-466f62209e6d">DRM_MSG_ACQUIRE_ISSUANCE_LICENSE_TEMPLATE</a> message that AD RMS sends to your callback function.

The template collection is saved in the template store of the local AD RMS store. Each template is stored in a file with the format TMP-<i>HashValue</i>-<i>TemplateGUID</i> where the hash value is a base64-encoded SHA-1 hash of server public key. You can call the <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a> function to enumerate the templates.

If properly configured, AD RMS clients can automatically obtain templates from the AD RMS server by using a WMI job in the task scheduler. Therefore, if WMI distribution is enabled, call <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a> to enumerate the rights policy templates from the local template store. Applications should avoid calling <b>DRMAcquireIssuanceLicenseTemplate</b> because the WMI job automatically copies templates to the client computer. However, <b>DRMAcquireIssuanceLicenseTemplate</b> can be used to retrieve templates from multiple servers, functionality not supported by the WMI job. You can also use it to retrieve templates if your application relies on a server lockbox. The WMI job is only available to applications that use a client lockbox.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/0d4ce794-8384-4f1c-bc8c-1e67fbb5f987">DRMAcquireLicense</a>
 

 


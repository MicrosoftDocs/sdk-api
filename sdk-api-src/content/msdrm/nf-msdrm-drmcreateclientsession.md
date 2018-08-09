---
UID: NF:msdrm.DRMCreateClientSession
title: DRMCreateClientSession function
author: windows-sdk-content
description: Creates a client session, which hosts license storage sessions and is used in activation and other function calls.
old-location: rm\drmcreateclientsession.htm
old-project: adrms_sdk
ms.assetid: 4b8928a0-1d72-47ee-a357-47fb5777d60c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DRMCreateClientSession, DRMCreateClientSession function [Active Directory Rights Management Services SDK 1.0], DRM_DEFAULTGROUPIDTYPE_PASSPORT, DRM_DEFAULTGROUPIDTYPE_WINDOWSAUTH, msdrm/DRMCreateClientSession, rm.drmcreateclientsession
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_SELECTIONSTYLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMCreateClientSession
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMCreateClientSession function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateClientSession</b> function creates a client session, which hosts license storage sessions and is used in activation and other function calls.


## -parameters




### -param pfnCallback [in]

A pointer to an application-defined callback function that will receive asynchronous function status messages in response to other AD RMS functions, such as <a href="https://msdn.microsoft.com/d3f4ac2c-95d9-4273-a679-81670dd62d28">DRMActivate</a>. The format of this callback function is defined in <a href="https://msdn.microsoft.com/41c200df-afbc-43a5-8046-d131fec3261a">Callback Prototype</a>. This parameter cannot be <b>NULL</b>.


### -param uCallbackVersion [in]

Specifies the version of the callback function. Currently, only version zero is supported.


### -param wszGroupIDProviderType [in]

A pointer to a null-terminated Unicode string that specifies the authentication type of the submitted <a href="r_gly.htm">rights account certificate</a> (RAC). This can be one of the following values.



#### DRM_DEFAULTGROUPIDTYPE_WINDOWSAUTH

Use Windows authentication. Specify this value also for an Active Directory Federation Services (ADFS) RAC.



#### DRM_DEFAULTGROUPIDTYPE_PASSPORT

Use Passport authentication.


### -param wszGroupID [in, optional]

A pointer to a null-terminated Unicode string that contains an email address for the user in the format <i>someone@example.com</i>. Typically, this value already exists in Active Directory (AD) and is the same ID as that supplied in the logon credentials. If it is not the same, later calls to <a href="https://msdn.microsoft.com/f6c7bc7f-e9e8-4fc4-b30f-31bc0f5f46aa">DRMIsActivated</a> and <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a> will fail. For more information, see Remarks.

Set this parameter to  <b>NULL</b> if you intend only to use the client session handle created by this function to retrieve a service location by calling <a href="https://msdn.microsoft.com/f7cbc3ba-009f-4a35-999e-139d41961fd9">DRMGetServiceLocation</a>.


### -param phClient [out]

A pointer to a <b>DRMHSESSION</b> value that receives the client session handle. When you have finished using the client session, close it by passing this handle to the <a href="https://msdn.microsoft.com/e948b31f-382c-4a32-8cc3-98df8c4a6db0">DRMCloseSession</a> function.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



If this function is successful, the AD RMS server returns a client session handle that is used by <a href="https://msdn.microsoft.com/d3f4ac2c-95d9-4273-a679-81670dd62d28">DRMActivate</a> to create a rights account certificate (RAC) in the license store for the new client session. The RAC is created by using the credentials of the logged–on user. If the email address specified in the <i>wszGroupID</i> parameter does not match that specified in the credentials, functions such as <a href="https://msdn.microsoft.com/f6c7bc7f-e9e8-4fc4-b30f-31bc0f5f46aa">DRMIsActivated</a> and <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a> that use information associated with the client session to search the license store for the RAC will fail.

For example, assume that  the user logged on by using cat@example.com but the <i>wszGroupID</i> parameter is set to dog@example.com. The RAC is created for cat@example.com. The <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a> function, however, searches the license store for a RAC that contains  dog@example.com and fails.

All license storage sessions must be closed before closing the client session. When you have finished using the client session, close it by passing the handle provided by this function to the <a href="https://msdn.microsoft.com/e948b31f-382c-4a32-8cc3-98df8c4a6db0">DRMCloseSession</a> function.

The <b>DRMCreateClientSession</b> function cannot be called concurrently by different processes running as different users on the same computer if one or more of these processes is a service process. A call by a second  process, for example, can succeed only after the client session handle for the first process has been closed.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/7d880b74-1934-4282-a7ca-1dac3602d6b4">Creating a Callback Function</a>



<a href="https://msdn.microsoft.com/e948b31f-382c-4a32-8cc3-98df8c4a6db0">DRMCloseSession</a>
 

 


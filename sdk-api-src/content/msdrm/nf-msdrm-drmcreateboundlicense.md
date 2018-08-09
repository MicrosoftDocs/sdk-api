---
UID: NF:msdrm.DRMCreateBoundLicense
title: DRMCreateBoundLicense function
author: windows-sdk-content
description: Allows an application to examine or exercise the rights on a locally stored license.
old-location: rm\drmcreateboundlicense.htm
old-project: adrms_sdk
ms.assetid: 102fa347-47be-4dc7-ba17-3f1ad3735b00
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DRMCreateBoundLicense, DRMCreateBoundLicense function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCreateBoundLicense, rm.drmcreateboundlicense
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
 - DRMCreateBoundLicense
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMCreateBoundLicense function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateBoundLicense</b> function allows an application to examine or exercise the rights on a locally stored license.


## -parameters




### -param hEnv [in]

A handle to an environment; the handle is created by using the <a href="https://msdn.microsoft.com/b46277f4-e854-4590-847a-cf4f878bee70">DRMInitEnvironment</a> function.


### -param pParams [in]

A pointer to a <a href="https://msdn.microsoft.com/25820f49-ffa8-40c4-87fc-ce4909ec20ed">DRMBOUNDLICENSEPARAMS</a> structure that specifies additional options; for more information, see the Remarks section. The principal specified here is the one the application will try to bind to. If you pass in <b>NULL</b> to identify the principal or rights group, the first principal or rights group in the license will be used.


### -param wszLicenseChain [in]

A pointer to a null-terminated Unicode string that contains the <a href="e_gly.htm">end-user license</a> (or license chain).


### -param phBoundLicense [out]

A pointer to a handle that receives the bound license. The <b>DRMHANDLE</b> passed back through <i>phBoundLicense</i> allows an application to navigate through all the license's objects (such as principals or rights) and attributes (such as maximum play count). A bound license consolidates duplicated rights information in the license and removes any rights information that is not available to the current user.


### -param phErrorLog [out]

This parameter must be <b>NULL</b>.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Calling this function binds a license to the right or rights specified in the  <a href="https://msdn.microsoft.com/25820f49-ffa8-40c4-87fc-ce4909ec20ed">DRMBOUNDLICENSEPARAMS</a> structure passed to the <i>pParams</i> parameter. If any right requested cannot be exercised by the current user, the function will fail. Note also that you must call <a href="https://msdn.microsoft.com/dcf95e9e-e2de-449e-a45a-4974094ecb7e">DRMSetMetaData</a> and specify a value for the <i>wszContentId</i> parameter before calling this function and that this value must be the same as the ID set in the <b>DRMBOUNDLICENSEPARAMS</b> structure or the function will fail.

If the function succeeds, it returns a handle to the bound license that can be examined, and also allows an application to exercise the bound right. This function does not decrement metered rights. Decrementing metered rights upon use is the responsibility of the application.

When license binding fails because of a missing or out of date revocation list, the return value does not indicate which license or certificate is causing the error. It could be the end-user license, the user's <a href="r_gly.htm">rights account certificate</a>, a <a href="c_gly.htm">client licensor certificate</a>, or another license or certificate. You must call <a href="https://msdn.microsoft.com/42c58096-429c-4278-b9ab-8c5a91361af8">DRMAcquireAdvisories</a> (and <a href="https://msdn.microsoft.com/819a8471-e447-4a4d-ae52-5929350df2c8">DRMRegisterRevocationList</a>) for each certificate until the error does not occur.

Principal authenticators required for a license must be loaded before calling this function. However, the authenticator can continue to function after the license is created.

When you have finished using the license handle, close it by calling the <a href="https://msdn.microsoft.com/422f286c-edf6-488f-8776-359ab2695be3">DRMCloseHandle</a> function. <b>DRMCloseHandle</b> closes the handle to the library and deletes the license from memory.


The handle returned by this function can be passed into one of the following functions to navigate deeper into the license hierarchy:

<ul>
<li>
<a href="https://msdn.microsoft.com/715fb3e6-6b1e-4136-9c25-efcde2015d6f">DRMGetBoundLicenseAttribute</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5b3814f5-bab7-4b46-a38b-54406cb8cae0">DRMGetBoundLicenseAttributeCount</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d1be0668-fb5a-4541-92dc-34255ba3fdad">DRMGetBoundLicenseObject</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1bb9a9b7-f254-4c2b-a7b0-5e9b99c92488">DRMGetBoundLicenseObjectCount</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/25820f49-ffa8-40c4-87fc-ce4909ec20ed">DRMBOUNDLICENSEPARAMS</a>
 

 


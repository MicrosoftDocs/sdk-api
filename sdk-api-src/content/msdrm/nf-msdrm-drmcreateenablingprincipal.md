---
UID: NF:msdrm.DRMCreateEnablingPrincipal
title: DRMCreateEnablingPrincipal function
author: windows-sdk-content
description: Creates an enabling principal needed to bind to a license.
old-location: rm\drmcreateenablingprincipal.htm
old-project: AdRms_Sdk
ms.assetid: 92858a46-cef5-4d25-9f3c-cbb343743565
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DRMCreateEnablingPrincipal, DRMCreateEnablingPrincipal function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCreateEnablingPrincipal, rm.drmcreateenablingprincipal
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
 - DRMCreateEnablingPrincipal
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMCreateEnablingPrincipal function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateEnablingPrincipal</b> function creates an enabling principal needed to bind to a license.


## -parameters




### -param hEnv [in]

A handle to an environment created by <a href="https://msdn.microsoft.com/b46277f4-e854-4590-847a-cf4f878bee70">DRMInitEnvironment</a>.


### -param hLibrary [in]

A handle to a library. Currently, the only valid library that can be used is the one passed out by <a href="https://msdn.microsoft.com/b46277f4-e854-4590-847a-cf4f878bee70">DRMInitEnvironment</a>.


### -param wszObject [in]

A pointer to a null-terminated Unicode string that specifies the enabling principal type. An application can use the object constants specified in Msdrmgetinfo.h.


### -param pidPrincipal [in]

A pointer to a <a href="https://msdn.microsoft.com/8b7f22e0-586e-4950-94fe-868b3fc91ffa">DRMID</a> structure that identifies the enabling principal. The <b>DRMID</b> members can be <b>NULL</b> to use the first principal in a license.


### -param wszCredentials [in]

A pointer to a null-terminated Unicode string that contains the <a href="r_gly.htm">rights account certificate</a> of the current user.


### -param phEnablingPrincipal

TBD




#### - pHEnablingPrincipal [out]

A pointer to a <b>DRMHANDLE</b> value that receives the created principal. Call <a href="https://msdn.microsoft.com/422f286c-edf6-488f-8776-359ab2695be3">DRMCloseHandle</a> to close the handle.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The enabling principal this function creates is used in the <a href="https://msdn.microsoft.com/25820f49-ffa8-40c4-87fc-ce4909ec20ed">DRMBOUNDLICENSEPARAMS</a> structure passed into <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a>. Call <a href="https://msdn.microsoft.com/422f286c-edf6-488f-8776-359ab2695be3">DRMCloseHandle</a> to close the enabling principal handle created by calling this function.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>
 

 


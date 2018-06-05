---
UID: NF:msdrm.DRMCloseQueryHandle
title: DRMCloseQueryHandle function
author: windows-sdk-content
description: Closes a handle to an unbound license object.
old-location: rm\drmclosequeryhandle.htm
old-project: AdRms_Sdk
ms.assetid: 4902a6e2-e3b2-4f05-970c-aa4f80895762
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DRMCloseQueryHandle, DRMCloseQueryHandle function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCloseQueryHandle, rm.drmclosequeryhandle
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msdrm.dll
api_name:
-	DRMCloseQueryHandle
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2  or later
---

# DRMCloseQueryHandle function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCloseQueryHandle</b> function closes a handle to an unbound license object.


## -parameters




### -param hQuery [in]

A handle to an object in an unbound license.


## -returns



 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The AD RMS system exposes an object-oriented interface to a license. Bound licenses are accessed using a <b>DRMHANDLE</b>, while unbound licenses are accessed by a <b>DRMQUERYHANDLE</b>. The two types are not interchangeable. This function closes unbound licenses. For more information about examining unbound licenses, see <a href="https://msdn.microsoft.com/2ae65ed2-7702-4e9b-b986-68b83ebe8bf5">DRMParseUnboundLicense</a>.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>
 

 


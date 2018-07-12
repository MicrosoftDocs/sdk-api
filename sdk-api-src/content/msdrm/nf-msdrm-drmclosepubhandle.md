---
UID: NF:msdrm.DRMClosePubHandle
title: DRMClosePubHandle function
author: windows-sdk-content
description: Closes a previously created DRMPUBHANDLE.
old-location: rm\drmclosepubhandle.htm
old-project: adrms_sdk
ms.assetid: a263a1a8-01b8-4ca6-aefb-f4374459c0c0
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: DRMClosePubHandle, DRMClosePubHandle function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMClosePubHandle, rm.drmclosepubhandle
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
 - DRMClosePubHandle
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMClosePubHandle function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMClosePubHandle</b> function closes a previously created <b>DRMPUBHANDLE</b>.


## -parameters




### -param hPub [in]

A handle to a publishing object.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



A <b>DRMPUBHANDLE</b> provides an opaque handle to many publishing objects. Creating, copying, and closing these handles with the appropriate Active Directory Rights Management function allows the AD RMS system to maintain a reference count on resources and free them appropriately, and also clears sensitive data from memory.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/3e031dec-ac80-4363-8786-2680d498cb5c">AD RMS Handles and Sessions</a>
 

 


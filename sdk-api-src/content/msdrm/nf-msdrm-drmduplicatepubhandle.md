---
UID: NF:msdrm.DRMDuplicatePubHandle
title: DRMDuplicatePubHandle function
author: windows-driver-content
description: Makes a copy of a DRMPUBHANDLE.
old-location: rm\drmduplicatepubhandle.htm
old-project: AdRms_Sdk
ms.assetid: 6bf94d17-ce09-492e-9b47-88cd54719d3e
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: DRMDuplicatePubHandle, DRMDuplicatePubHandle function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMDuplicatePubHandle, rm.drmduplicatepubhandle
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
req.typenames: TF_SELECTIONSTYLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msdrm.dll
api_name:
-	DRMDuplicatePubHandle
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMDuplicatePubHandle function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMDuplicatePubHandle</b> function makes a copy of a <b>DRMPUBHANDLE</b>.


## -parameters




### -param hPubIn [in]

The <b>DRMPUBHANDLE</b> to make a copy of.


### -param phPubOut [out]

A pointer to a <b>DRMPUBHANDLE</b> value that receives the duplicate handle. When this handle is no longer needed, release it  by passing it to the <a href="https://msdn.microsoft.com/a263a1a8-01b8-4ca6-aefb-f4374459c0c0">DRMClosePubHandle</a> function.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Using the appropriate function to create, copy, and close these handles allows Active Directory Rights Management Services to maintain a reference count on resources and free them appropriately; it also clears sensitive data from memory.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/a263a1a8-01b8-4ca6-aefb-f4374459c0c0">DRMClosePubHandle</a>
 

 


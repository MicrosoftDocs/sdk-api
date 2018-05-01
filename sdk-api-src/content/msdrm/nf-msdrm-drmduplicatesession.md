---
UID: NF:msdrm.DRMDuplicateSession
title: DRMDuplicateSession function
author: windows-driver-content
description: Duplicates a client or license storage session.
old-location: rm\drmduplicatesession.htm
old-project: AdRms_Sdk
ms.assetid: 4a768919-36aa-4e09-898f-bd8f9c21cb0e
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: DRMDuplicateSession, DRMDuplicateSession function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMDuplicateSession, rm.drmduplicatesession
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
-	DRMDuplicateSession
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMDuplicateSession function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMDuplicateSession</b> function duplicates a client or license storage session.


## -parameters




### -param hSessionIn [in]

A handle to a session to duplicate.


### -param phSessionOut [out]

Pointer to the duplicated session handle. Call <a href="https://msdn.microsoft.com/e948b31f-382c-4a32-8cc3-98df8c4a6db0">DRMCloseSession</a> to close the handle.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Creating, copying, and closing handles with the appropriate function allows the rights management system to maintain a reference count on resources and free them appropriately, and also clears sensitive data from memory. Call <a href="https://msdn.microsoft.com/e948b31f-382c-4a32-8cc3-98df8c4a6db0">DRMCloseSession</a> to close the handle created by calling this function.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>
 

 


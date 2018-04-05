---
UID: NF:msdrm.DRMGetUsers
title: DRMGetUsers function
author: windows-driver-content
description: Retrieves a specific user from an issuance license.
old-location: rm\drmgetusers.htm
old-project: AdRms_Sdk
ms.assetid: 4c8c8249-2e90-4eea-9a3b-dd7d9970ba98
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: DRMGetUsers, DRMGetUsers function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetUsers, rm.drmgetusers
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
-	DRMGetUsers
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMGetUsers function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetUsers</b> function retrieves a specific user from an issuance license.


## -parameters




### -param hIssuanceLicense [in]

The handle of the issuance license to retrieve the user from.


### -param uIndex [in]

The zero-based index of the user in the issuance license to retrieve. To enumerate all the users in the issuance license, create a loop starting at zero and incrementing by one. When the function returns <b>E_DRM_NO_MORE_DATA</b>, there are no more users in the issuance license.


### -param phUser [out]

A pointer to a <b>DRMPUBHANDLE</b> value that receives the handle to the requested user. Call <a href="https://msdn.microsoft.com/a263a1a8-01b8-4ca6-aefb-f4374459c0c0">DRMClosePubHandle</a> to close the handle.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



To enumerate all the users in the issuance license, create a loop starting at zero and incrementing by one. When the function returns <b>E_DRM_NO_MORE_DATA</b>, there are no more users in the issuance license.  Call <a href="https://msdn.microsoft.com/a263a1a8-01b8-4ca6-aefb-f4374459c0c0">DRMClosePubHandle</a> to close the user handle created by calling this function.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/98c0640d-8ee1-4072-989d-16a2e8ba09b3">DRMGetUserInfo</a>



<a href="https://msdn.microsoft.com/46191a8e-66e1-44a5-8052-a21fda88625a">DRMGetUserRights</a>
 

 


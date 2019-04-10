---
UID: NF:msdrm.DRMGetUserRights
title: DRMGetUserRights function (msdrm.h)
author: windows-sdk-content
description: Retrieves user/right pairs from an issuance license.
old-location: rm\drmgetuserrights.htm
tech.root: AdRms_Sdk
ms.assetid: 46191a8e-66e1-44a5-8052-a21fda88625a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DRMGetUserRights, DRMGetUserRights function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetUserRights, rm.drmgetuserrights
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
 - DRMGetUserRights
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMGetUserRights function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetUserRights</b> function retrieves user/right pairs from an issuance license.


## -parameters




### -param hIssuanceLicense [in]

The handle of the issuance license to retrieve the user rights from.


### -param hUser [in]

The handle of a user in the issuance license to retrieve the rights for.


### -param uIndex [in]

The zero-based index that indicates which right to retrieve for the specified user. To enumerate all the rights assigned to a user in the issuance license, create a loop starting at zero and incrementing by one. When the function returns <b>E_DRM_NO_MORE_DATA</b>, there are no more rights assigned to that user.


### -param phRight [out]

A pointer to a <b>DRMPUBHANDLE</b> value that receives the handle to the requested right. Call <a href="https://msdn.microsoft.com/a263a1a8-01b8-4ca6-aefb-f4374459c0c0">DRMClosePubHandle</a> to close the handle.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This function gets a right associated with a specific user. User rights are added by using the function <a href="https://msdn.microsoft.com/10b76b20-cee7-44f3-b9bd-2b690fdd040c">DRMAddRightWithUser</a>. To enumerate all rights assigned to a user, pass in a user handle and an index value of zero. Continue to call this function, incrementing the index number by one each time, until <b>E_DRM_NO_MORE_DATA</b> is returned.

Call <a href="https://msdn.microsoft.com/a263a1a8-01b8-4ca6-aefb-f4374459c0c0">DRMClosePubHandle</a> to close the handle created by calling this function.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/10b76b20-cee7-44f3-b9bd-2b690fdd040c">DRMAddRightWithUser</a>



<a href="https://msdn.microsoft.com/4c8c8249-2e90-4eea-9a3b-dd7d9970ba98">DRMGetUsers</a>
 

 


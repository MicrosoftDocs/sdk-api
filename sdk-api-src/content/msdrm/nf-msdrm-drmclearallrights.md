---
UID: NF:msdrm.DRMClearAllRights
title: DRMClearAllRights function
author: windows-driver-content
description: Removes all rights from an existing issuance license.
old-location: rm\drmclearallrights.htm
old-project: AdRms_Sdk
ms.assetid: f0a5dc8d-2bc6-4fcc-8871-ea80fc6a4abc
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: DRMClearAllRights, DRMClearAllRights function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMClearAllRights, rm.drmclearallrights
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
-	DRMClearAllRights
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMClearAllRights function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMClearAllRights</b> function removes all rights from an existing issuance license.


## -parameters




### -param hIssuanceLicense [in]

A handle to the issuance license to remove the rights from.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



There is no way to remove individual rights from an issuance license.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/10b76b20-cee7-44f3-b9bd-2b690fdd040c">DRMAddRightWithUser</a>
 

 


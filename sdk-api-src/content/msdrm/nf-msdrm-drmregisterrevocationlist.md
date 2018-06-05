---
UID: NF:msdrm.DRMRegisterRevocationList
title: DRMRegisterRevocationList function
author: windows-sdk-content
description: Registers a rights revocation list on the client.
old-location: rm\drmregisterrevocationlist.htm
old-project: AdRms_Sdk
ms.assetid: 819a8471-e447-4a4d-ae52-5929350df2c8
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DRMRegisterRevocationList, DRMRegisterRevocationList function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMRegisterRevocationList, rm.drmregisterrevocationlist
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
-	DRMRegisterRevocationList
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMRegisterRevocationList function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMRegisterRevocationList</b> function registers a rights revocation list on the client.


## -parameters




### -param hEnv [in]

A handle to an environment, created by <a href="https://msdn.microsoft.com/b46277f4-e854-4590-847a-cf4f878bee70">DRMInitEnvironment</a>.


### -param wszRevocationList [in]

Revocation list as a null-terminated string.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



A revocation list holds all group identities, end-user licenses, or other principals that have been revoked. This function blocks the display of content from distributors or users whose license has been revoked. When an attempt to bind to a license fails with <b>E_DRM_BIND_REVOCATION_LIST_STALE</b> or <b>E_DRM_BIND_NO_APPLICABLE_REVOCATION_LIST</b>, this indicates that the license requires a revocation list. This list must either be found in the license store (using <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a>) or must be acquired fresh using <a href="https://msdn.microsoft.com/42c58096-429c-4278-b9ab-8c5a91361af8">DRMAcquireAdvisories</a> and then retrieved from the license store. Registration is only for the lifetime of the environment passed in. Any time that a new environment object is created, the necessary revocation lists must be registered for that environment.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/42c58096-429c-4278-b9ab-8c5a91361af8">DRMAcquireAdvisories</a>



<a href="https://msdn.microsoft.com/1e1a7cfc-8445-4d0c-bc45-310fa9364839">Revoking a Certificate</a>
 

 


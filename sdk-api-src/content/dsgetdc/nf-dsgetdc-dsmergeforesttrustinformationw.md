---
UID: NF:dsgetdc.DsMergeForestTrustInformationW
title: DsMergeForestTrustInformationW function (dsgetdc.h)
author: windows-sdk-content
description: Merges the changes from a new forest trust data structure with an old forest trust data structure.
old-location: ad\dsmergeforesttrustinformationw.htm
tech.root: ad
ms.assetid: f42e16d0-62b2-49c4-b182-d1e744afe58c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DsMergeForestTrustInformationW, DsMergeForestTrustInformationW function [Active Directory], ad.dsmergeforesttrustinformationw, dsgetdc/DsMergeForestTrustInformationW
ms.topic: function
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - DsMergeForestTrustInformationW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsMergeForestTrustInformationW function


## -description


The <b>DsMergeForestTrustInformationW</b> function merges the changes from a new forest trust data structure with an old forest trust data structure.


## -parameters




### -param DomainName [in]

Pointer to a null-terminated Unicode string that specifies the trusted domain to  update.


### -param NewForestTrustInfo [in]

Pointer to an <b>LSA_FOREST_TRUST_INFORMATION</b> structure that contains the new forest trust data to be merged.
        The <b>Flags</b> and <b>Time</b> members of the entries are ignored.


### -param OldForestTrustInfo [in, optional]

Pointer to an <b>LSA_FOREST_TRUST_INFORMATION</b> structure that contains the old forest trust data to be merged.
        This parameter may be <b>NULL</b> if no records exist.


### -param MergedForestTrustInfo [out]

Pointer to an <b>LSA_FOREST_TRUST_INFORMATION</b> structure pointer that receives the merged forest trust data.

The caller must free this structure when it is no longer required by calling <a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>.


## -returns



Returns <b>NO_ERROR</b> if successful or a Windows error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/7b519c81-5a6c-470a-a525-1894efd53305">Directory Service Functions</a>



<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>
 

 


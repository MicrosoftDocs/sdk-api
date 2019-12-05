---
UID: NF:ntdsapi.DsFreeNameResultA
title: DsFreeNameResultA function (ntdsapi.h)
description: Frees the memory held by a DS_NAME_RESULT structure.
old-location: ad\dsfreenameresult.htm
tech.root: ad
ms.assetid: 210650a6-70b9-4d4f-b99a-106afd3fe615
ms.date: 12/05/2018
ms.keywords: DsFreeNameResult, DsFreeNameResult function [Active Directory], DsFreeNameResultA, DsFreeNameResultW, _glines_dsfreenameresult, ad.dsfreenameresult, ntdsapi/DsFreeNameResult, ntdsapi/DsFreeNameResultA, ntdsapi/DsFreeNameResultW
ms.topic: function
f1_keywords:
- ntdsapi/DsFreeNameResult
dev_langs:
- c++
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsFreeNameResultW (Unicode) and DsFreeNameResultA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ntdsapi.dll
- API-MS-Win-Security-ActiveDirectoryClient-l1-1-0.dll
- KernelBase.dll
- API-Ms-Win-Security-ActiveDirectoryClient-L1-1-1.dll
api_name:
- DsFreeNameResult
- DsFreeNameResultA
- DsFreeNameResultW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DsFreeNameResultA function


## -description


The <b>DsFreeNameResult</b> function frees the memory held by a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure. Use this function to free the memory allocated by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a> function.


## -parameters




### -param pResult

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure to be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa">DsCrackNames</a>
 

 


---
UID: NS:ntdsapi._DS_REPL_KCC_DSA_FAILURESW
title: "_DS_REPL_KCC_DSA_FAILURESW"
author: windows-sdk-content
description: The DS_REPL_KCC_DSA_FAILURES structure contains an array of DS_REPL_KCC_DSA_FAILURE structures, which in turn contain replication state data with respect to inbound replication partners, as returned by the DsReplicaGetInfo and DsReplicaGetInfo2 functions.
old-location: ad\ds_repl_kcc_dsa_failures.htm
old-project: ad
ms.assetid: bb011502-38ae-43b7-a6ad-de16b499f61b
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: DS_REPL_KCC_DSA_FAILURES, DS_REPL_KCC_DSA_FAILURES structure [Active Directory], DS_REPL_KCC_DSA_FAILURESW, _DS_REPL_KCC_DSA_FAILURESW, _glines_ds_repl_kcc_dsa_failures, ad.ds__repl__kcc__dsa__failures, ad.ds_repl_kcc_dsa_failures, ntdsapi/DS_REPL_KCC_DSA_FAILURES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntdsapi.h
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
tech.root: 
req.typenames: DS_REPL_KCC_DSA_FAILURESW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_REPL_KCC_DSA_FAILURES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _DS_REPL_KCC_DSA_FAILURESW structure


## -description


The <b>DS_REPL_KCC_DSA_FAILURES</b> structure contains an array of <a href="https://msdn.microsoft.com/7a7131ce-a647-4b3d-a9f3-091b6dcebff7">DS_REPL_KCC_DSA_FAILURE</a> structures, which in turn contain replication state data with respect to inbound replication partners, as returned by the 
<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> and <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> functions.


## -struct-fields




### -field cNumEntries

Contains the number of elements in the <b>rgMetaData</b> array.


### -field dwReserved

Reserved for future use.


### -field rgDsaFailure.size_is

 


### -field rgDsaFailure.size_is.cNumEntries

 


### -field rgDsaFailure

Contains an array of <a href="https://msdn.microsoft.com/7a7131ce-a647-4b3d-a9f3-091b6dcebff7">DS_REPL_KCC_DSA_FAILURE</a> structures that contain the requested replication data. The <b>cNumEntries</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/7a7131ce-a647-4b3d-a9f3-091b6dcebff7">DS_REPL_KCC_DSA_FAILURE</a>



<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 


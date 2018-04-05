---
UID: NF:ntdsapi.DsFreeSpnArrayA
title: DsFreeSpnArrayA function
author: windows-driver-content
description: Frees an array returned from the DsGetSpn function.
old-location: ad\dsfreespnarray.htm
old-project: AD
ms.assetid: 1c229933-432d-4ded-be3b-3bd339a0abe4
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: DsFreeSpnArray, DsFreeSpnArray function [Active Directory], DsFreeSpnArrayA, DsFreeSpnArrayW, _glines_dsfreespnarray, ad.dsfreespnarray, ntdsapi/DsFreeSpnArray, ntdsapi/DsFreeSpnArrayA, ntdsapi/DsFreeSpnArrayW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsFreeSpnArrayW (Unicode) and DsFreeSpnArrayA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DS_REPL_OP_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntdsapi.dll
api_name:
-	DsFreeSpnArray
-	DsFreeSpnArrayA
-	DsFreeSpnArrayW
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# DsFreeSpnArrayA function


## -description


The <b>DsFreeSpnArray</b> function frees an array returned from the 
<a href="https://msdn.microsoft.com/cbd53850-9b05-4f74-ab07-30dcad583fc5">DsGetSpn</a> function.


## -parameters




### -param cSpn [in]

Specifies the number of elements contained in <i>rpszSpn</i>.


### -param rpszSpn [in]

Pointer to an array returned from <a href="https://msdn.microsoft.com/cbd53850-9b05-4f74-ab07-30dcad583fc5">DsGetSpn</a>.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/cbd53850-9b05-4f74-ab07-30dcad583fc5">DsGetSpn</a>
 

 


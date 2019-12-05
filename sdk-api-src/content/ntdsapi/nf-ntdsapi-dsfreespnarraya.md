---
UID: NF:ntdsapi.DsFreeSpnArrayA
title: DsFreeSpnArrayA function (ntdsapi.h)
description: Frees an array returned from the DsGetSpn function.
old-location: ad\dsfreespnarray.htm
tech.root: ad
ms.assetid: 1c229933-432d-4ded-be3b-3bd339a0abe4
ms.date: 12/05/2018
ms.keywords: DsFreeSpnArray, DsFreeSpnArray function [Active Directory], DsFreeSpnArrayA, DsFreeSpnArrayW, _glines_dsfreespnarray, ad.dsfreespnarray, ntdsapi/DsFreeSpnArray, ntdsapi/DsFreeSpnArrayA, ntdsapi/DsFreeSpnArrayW
ms.topic: function
f1_keywords:
- ntdsapi/DsFreeSpnArray
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
req.unicode-ansi: DsFreeSpnArrayW (Unicode) and DsFreeSpnArrayA (ANSI)
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
api_name:
- DsFreeSpnArray
- DsFreeSpnArrayA
- DsFreeSpnArrayW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DsFreeSpnArrayA function


## -description


The <b>DsFreeSpnArray</b> function frees an array returned from the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetspna">DsGetSpn</a> function.


## -parameters




### -param cSpn [in]

Specifies the number of elements contained in <i>rpszSpn</i>.


### -param rpszSpn [in]

Pointer to an array returned from <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetspna">DsGetSpn</a>.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetspna">DsGetSpn</a>
 

 


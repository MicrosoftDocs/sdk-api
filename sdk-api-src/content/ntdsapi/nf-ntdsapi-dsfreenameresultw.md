---
UID: NF:ntdsapi.DsFreeNameResultW
title: DsFreeNameResultW function
author: windows-sdk-content
description: Frees the memory held by a DS_NAME_RESULT structure.
old-location: ad\dsfreenameresult.htm
old-project: AD
ms.assetid: 210650a6-70b9-4d4f-b99a-106afd3fe615
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DsFreeNameResult, DsFreeNameResult function [Active Directory], DsFreeNameResultA, DsFreeNameResultW, _glines_dsfreenameresult, ad.dsfreenameresult, ntdsapi/DsFreeNameResult, ntdsapi/DsFreeNameResultA, ntdsapi/DsFreeNameResultW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: DS_REPL_OP_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntdsapi.dll
-	API-MS-Win-Security-ActiveDirectoryClient-l1-1-0.dll
-	KernelBase.dll
-	API-Ms-Win-Security-ActiveDirectoryClient-L1-1-1.dll
api_name:
-	DsFreeNameResult
-	DsFreeNameResultA
-	DsFreeNameResultW
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# DsFreeNameResultW function


## -description


The <b>DsFreeNameResult</b> function frees the memory held by a 
<a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a> structure. Use this function to free the memory allocated by the 
<a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a> function.


## -parameters




### -param pResult

Pointer to the <a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a> structure to be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a>
 

 


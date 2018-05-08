---
UID: NF:gpmgmt.IGPMRSOP.CreateQueryResults
title: IGPMRSOP::CreateQueryResults
author: windows-driver-content
description: Executes a Resultant Set of Policy (RSoP) query.
old-location: gpmc\igpmrsop_createqueryresults.htm
old-project: GPMC
ms.assetid: 2259a014-3ecb-480d-ab65-9d27c0acf26c
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: CreateQueryResults, CreateQueryResults method [GPMC], CreateQueryResults method [GPMC],GPMRSOP object, CreateQueryResults method [GPMC],IGPMRSOP interface, GPMRSOP object [GPMC],CreateQueryResults method, IGPMRSOP interface [GPMC],CreateQueryResults method, IGPMRSOP.CreateQueryResults, IGPMRSOP::CreateQueryResults, _win32_igpmrsop_createqueryresults, gpmc.igpmrsop_createqueryresults, gpmgmt/IGPMRSOP::CreateQueryResults
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMRSOP.CreateQueryResults
-	GPMRSOP.CreateQueryResults
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMRSOP::CreateQueryResults


## -description


Executes a Resultant Set of Policy (RSoP) query. The method supports both logging mode and planning mode queries. Before calling this method, set the appropriate logging mode or planning mode properties. For more information and a list of properties, see 
<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">IGPMRSOP Property Methods</a>. RSoP planning mode requires a domain controller running Windows Server to perform the query.


## -parameters






## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -remarks



Call the 
<a href="https://msdn.microsoft.com/c2bf9050-4db0-4bf0-a063-0076ba191ff6">IGPMRSOP::ReleaseQueryResults</a> method to release the WMI namespace created by this method.

In the GPMC UI, logging mode is also referred to as "Group Policy Results", and planning mode is also referred to as "Group Policy Modeling".




## -see-also




<a href="https://msdn.microsoft.com/86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3">IGPMRSOP</a>
 

 


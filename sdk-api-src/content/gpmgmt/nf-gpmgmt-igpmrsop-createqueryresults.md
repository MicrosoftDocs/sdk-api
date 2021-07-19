---
UID: NF:gpmgmt.IGPMRSOP.CreateQueryResults
title: IGPMRSOP::CreateQueryResults (gpmgmt.h)
description: Executes a Resultant Set of Policy (RSoP) query.
helpviewer_keywords: ["CreateQueryResults","CreateQueryResults method [GPMC]","CreateQueryResults method [GPMC]","GPMRSOP object","CreateQueryResults method [GPMC]","IGPMRSOP interface","GPMRSOP object [GPMC]","CreateQueryResults method","IGPMRSOP interface [GPMC]","CreateQueryResults method","IGPMRSOP.CreateQueryResults","IGPMRSOP::CreateQueryResults","_win32_igpmrsop_createqueryresults","gpmc.igpmrsop_createqueryresults","gpmgmt/IGPMRSOP::CreateQueryResults"]
old-location: gpmc\igpmrsop_createqueryresults.htm
tech.root: gpmc
ms.assetid: 2259a014-3ecb-480d-ab65-9d27c0acf26c
ms.date: 12/05/2018
ms.keywords: CreateQueryResults, CreateQueryResults method [GPMC], CreateQueryResults method [GPMC],GPMRSOP object, CreateQueryResults method [GPMC],IGPMRSOP interface, GPMRSOP object [GPMC],CreateQueryResults method, IGPMRSOP interface [GPMC],CreateQueryResults method, IGPMRSOP.CreateQueryResults, IGPMRSOP::CreateQueryResults, _win32_igpmrsop_createqueryresults, gpmc.igpmrsop_createqueryresults, gpmgmt/IGPMRSOP::CreateQueryResults
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
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMRSOP::CreateQueryResults
 - gpmgmt/IGPMRSOP::CreateQueryResults
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMRSOP.CreateQueryResults
 - GPMRSOP.CreateQueryResults
---

# IGPMRSOP::CreateQueryResults


## -description

Executes a Resultant Set of Policy (RSoP) query. The method supports both logging mode and planning mode queries. Before calling this method, set the appropriate logging mode or planning mode properties. For more information and a list of properties, see 
<a href="/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">IGPMRSOP Property Methods</a>. RSoP planning mode requires a domain controller running Windows Server to perform the query.



## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -remarks

Call the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmrsop-releasequeryresults">IGPMRSOP::ReleaseQueryResults</a> method to release the WMI namespace created by this method.

In the GPMC UI, logging mode is also referred to as "Group Policy Results", and planning mode is also referred to as "Group Policy Modeling".

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmrsop">IGPMRSOP</a>

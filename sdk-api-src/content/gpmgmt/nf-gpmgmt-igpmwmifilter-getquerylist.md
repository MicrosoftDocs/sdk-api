---
UID: NF:gpmgmt.IGPMWMIFilter.GetQueryList
title: IGPMWMIFilter::GetQueryList (gpmgmt.h)
description: Retrieves the query list stored in the WMI filter.
helpviewer_keywords: ["GPMWMIFilter class [GPMC]","GetQueryList method","GetQueryList","GetQueryList method [GPMC]","GetQueryList method [GPMC]","GPMWMIFilter class","GetQueryList method [GPMC]","IGPMWMIFilter interface","IGPMWMIFilter interface [GPMC]","GetQueryList method","IGPMWMIFilter.GetQueryList","IGPMWMIFilter::GetQueryList","_win32_igpmwmifilter_getquerylist","gpmc.igpmwmifilter_getquerylist","gpmgmt/IGPMWMIFilter::GetQueryList"]
old-location: gpmc\igpmwmifilter_getquerylist.htm
tech.root: gpmc
ms.assetid: ea20dc00-fb6d-44dc-81ad-e9aa2040f3ed
ms.date: 12/05/2018
ms.keywords: GPMWMIFilter class [GPMC],GetQueryList method, GetQueryList, GetQueryList method [GPMC], GetQueryList method [GPMC],GPMWMIFilter class, GetQueryList method [GPMC],IGPMWMIFilter interface, IGPMWMIFilter interface [GPMC],GetQueryList method, IGPMWMIFilter.GetQueryList, IGPMWMIFilter::GetQueryList, _win32_igpmwmifilter_getquerylist, gpmc.igpmwmifilter_getquerylist, gpmgmt/IGPMWMIFilter::GetQueryList
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
 - IGPMWMIFilter::GetQueryList
 - gpmgmt/IGPMWMIFilter::GetQueryList
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
 - IGPMWMIFilter.GetQueryList
 - GPMWMIFilter.GetQueryList
---

# IGPMWMIFilter::GetQueryList


## -description

Retrieves the query list stored in the WMI filter.

## -parameters

### -param pQryList [out]

Pointer to a <b>SAFEARRAY</b> of <b>VARIANT</b> members that contain the <b>BSTR </b> strings representing the queries. Each  <b>BSTR</b> string contains the query string along with the namespace information for that query.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
An array of strings representing the queries. Each string contains the query string along with the namespace information for that query.

<h3>VB</h3>
An array of strings representing the queries. Each string contains the query string along with the namespace information for that query.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">IGPMWMIFilterCollection</a>
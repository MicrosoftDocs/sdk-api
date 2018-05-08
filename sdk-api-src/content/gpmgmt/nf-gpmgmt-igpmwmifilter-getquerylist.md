---
UID: NF:gpmgmt.IGPMWMIFilter.GetQueryList
title: IGPMWMIFilter::GetQueryList
author: windows-driver-content
description: Retrieves the query list stored in the WMI filter.
old-location: gpmc\igpmwmifilter_getquerylist.htm
old-project: GPMC
ms.assetid: ea20dc00-fb6d-44dc-81ad-e9aa2040f3ed
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GPMWMIFilter class [GPMC],GetQueryList method, GetQueryList, GetQueryList method [GPMC], GetQueryList method [GPMC],GPMWMIFilter class, GetQueryList method [GPMC],IGPMWMIFilter interface, IGPMWMIFilter interface [GPMC],GetQueryList method, IGPMWMIFilter.GetQueryList, IGPMWMIFilter::GetQueryList, _win32_igpmwmifilter_getquerylist, gpmc.igpmwmifilter_getquerylist, gpmgmt/IGPMWMIFilter::GetQueryList
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
-	IGPMWMIFilter.GetQueryList
-	GPMWMIFilter.GetQueryList
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMWMIFilter::GetQueryList


## -description


Retrieves the query list stored in the WMI filter.


## -parameters




### -param pQryList [out]

Pointer to a <b>SAFEARRAY</b> of <b>VARIANT</b> members that contain the <b>BSTR </b>strings representing the queries. Each  <b>BSTR</b> string contains the query string along with the namespace information for that query.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
An array of strings representing the queries. Each string contains the query string along with the namespace information for that query.

<h3>VB</h3>
An array of strings representing the queries. Each string contains the query string along with the namespace information for that query.




## -see-also




<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">IGPMWMIFilter</a>



<a href="https://msdn.microsoft.com/8f65e6f6-fca3-46b7-aa0d-804470feb5bb">IGPMWMIFilterCollection</a>
 

 


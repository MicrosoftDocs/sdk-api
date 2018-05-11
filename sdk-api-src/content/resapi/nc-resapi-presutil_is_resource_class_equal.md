---
UID: NC:resapi.PRESUTIL_IS_RESOURCE_CLASS_EQUAL
title: PRESUTIL_IS_RESOURCE_CLASS_EQUAL
author: windows-driver-content
description: Tests whether the resource class of a specified resource is equal to a specified resource class. The PRESUTIL_IS_RESOURCE_CLASS_EQUAL type defines a pointer to this function.
old-location: mscs\resutilisresourceclassequal.htm
old-project: MsCS
ms.assetid: 3200abd3-5f95-48c5-acd9-8094c0072039
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: PRESUTIL_IS_RESOURCE_CLASS_EQUAL, PRESUTIL_IS_RESOURCE_CLASS_EQUAL callback, PRESUTIL_IS_RESOURCE_CLASS_EQUAL callback function [Failover Cluster], _wolf_resutilisresourceclassequal, mscs.resutilisresourceclassequal, resapi/PRESUTIL_IS_RESOURCE_CLASS_EQUAL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	PRESUTIL_IS_RESOURCE_CLASS_EQUAL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PRESUTIL_IS_RESOURCE_CLASS_EQUAL callback function


## -description


Tests whether the resource class of a specified  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> is equal to a specified resource class. The <b>PRESUTIL_IS_RESOURCE_CLASS_EQUAL</b> type defines a pointer to this function.


## -parameters




### -param prci [in]

Pointer to a  <a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a> structure describing the resource class.


### -param hResource [in]

Handle to the resource whose class is to be compared to <i>prci</i>.


## -returns



If the resource classes are equal, the function returns <b>TRUE</b>.

If the resource classes are not equal, 
the function returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/a34bbe15-f13f-4034-b2f1-fea3e58c579e">ResUtilResourcesEqual</a>
 

 


---
UID: NC:clusapi.PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET
title: PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET
author: windows-driver-content
description: Closes an open enumeration for a groupset.
old-location: mscs\clustergroupcollectioncloseenum.htm
old-project: MsCS
ms.assetid: b82e13f0-364c-41cf-9fda-98a95f23ff7d
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET, PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET callback, PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET callback function [Failover Cluster], clusapi/PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET, mscs.clustergroupcollectioncloseenum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLOSE_CLUSTER_GROUP_GROUPSET callback function


## -description


Closes an open enumeration for a groupset.


## -parameters




### -param hGroupSet








#### - hGroupCollectionEnum [in]

The enumeration to be closed.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




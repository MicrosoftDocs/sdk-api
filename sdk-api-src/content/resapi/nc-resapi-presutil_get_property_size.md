---
UID: NC:resapi.PRESUTIL_GET_PROPERTY_SIZE
title: PRESUTIL_GET_PROPERTY_SIZE
author: windows-driver-content
description: Returns the total number of bytes required for a specified property.
old-location: mscs\resutilgetpropertysize.htm
old-project: MsCS
ms.assetid: 0f21ef2b-747c-4fb3-a13c-16bcb7bfd46e
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PRESUTIL_GET_PROPERTY_SIZE, PRESUTIL_GET_PROPERTY_SIZE callback function [Failover Cluster], _wolf_resutilgetpropertysize, mscs.resutilgetpropertysize, resapi/PRESUTIL_GET_PROPERTY_SIZE
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
-	PRESUTIL_GET_PROPERTY_SIZE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PRESUTIL_GET_PROPERTY_SIZE callback


## -description


Returns the total number of bytes required for a specified property.


## -parameters




### -param hkeyClusterKey [in]


<a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">Cluster database</a> key identifying the location of the property to size.


### -param pPropertyTableItem [in]

Pointer to a  <a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a> structure describing the property to size.


### -param pcbOutPropertyListSize [in, out]

Pointer to the total number of bytes required for the property value, which includes the  <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure and the data.


### -param pnPropertyCount [in, out]

Pointer to the total number of properties. This value is incremented to include this property if  <i>ResUtilGetPropertySize</i> is successful.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error codes.




## -see-also




<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>
 

 


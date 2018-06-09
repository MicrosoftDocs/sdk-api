---
UID: NC:resapi.PRESUTIL_GET_PROPERTY_FORMATS
title: PRESUTIL_GET_PROPERTY_FORMATS
author: windows-sdk-content
description: Returns a property format list describing the format of a specified set of properties. The PRESUTIL_GET_PROPERTY_FORMATS type defines a pointer to this function.
old-location: mscs\resutilgetpropertyformats.htm
old-project: MsCS
ms.assetid: 034c7a4f-4219-47ea-afb0-a7c634d1b544
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: PRESUTIL_GET_PROPERTY_FORMATS, PRESUTIL_GET_PROPERTY_FORMATS callback, PRESUTIL_GET_PROPERTY_FORMATS callback function [Failover Cluster], _wolf_resutilgetpropertyformats, mscs.resutilgetpropertyformats, resapi/PRESUTIL_GET_PROPERTY_FORMATS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - PRESUTIL_GET_PROPERTY_FORMATS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PRESUTIL_GET_PROPERTY_FORMATS callback function


## -description


Returns a property format list describing the format of a specified set of properties. The <b>PRESUTIL_GET_PROPERTY_FORMATS</b> type defines a pointer to this function.


## -parameters




### -param pPropertyTable [in]

Pointer to a <a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a> property 
       table specifying the properties whose formats are to be retrieved.


### -param pOutPropertyFormatList [out]

On input, pointer to a buffer. On a successful return, pointer to a property format list describing the 
       format of each property specified by <i>pPropertyTable</i>.


### -param cbPropertyFormatListSize [in]

Specifies the allocated size (in bytes) of the buffer pointed to by 
       <i>pOutPropertyFormatList</i>.


### -param pcbBytesReturned [out]

Pointer to the actual size (in bytes) of the property format list that results from the operation.


### -param pcbRequired [out]

If the buffer pointed to by the <i>pOutPropertyFormatList</i> parameter is too small to 
       hold the resulting data, <i>pcbRequired</i> points to the required buffer size (in 
       bytes).


## -returns



Returns <b>ERROR_SUCCESS</b> if the operation was successful.




## -see-also




<a href="https://msdn.microsoft.com/29f87a9c-98e2-46c0-94a0-634924e07930">CLUSCTL_CLUSTER_GET_COMMON_PROPERTY_FMTS</a>



<a href="https://msdn.microsoft.com/03ba13be-39ea-4352-8218-18f4ed52bd99">General Utility Functions</a>



<a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>
 

 


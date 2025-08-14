---
UID: NF:resapi.ResUtilGetPropertyFormats
title: ResUtilGetPropertyFormats function (resapi.h)
description: Returns a property format list describing the format of a specified set of properties. The PRESUTIL_GET_PROPERTY_FORMATS type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_PROPERTY_FORMATS","PRESUTIL_GET_PROPERTY_FORMATS function [Failover Cluster]","ResUtilGetPropertyFormats","ResUtilGetPropertyFormats function [Failover Cluster]","_wolf_resutilgetpropertyformats","mscs.resutilgetpropertyformats","resapi/PRESUTIL_GET_PROPERTY_FORMATS","resapi/ResUtilGetPropertyFormats"]
old-location: mscs\resutilgetpropertyformats.htm
tech.root: MsCS
ms.assetid: 034c7a4f-4219-47ea-afb0-a7c634d1b544
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_PROPERTY_FORMATS, PRESUTIL_GET_PROPERTY_FORMATS function [Failover Cluster], ResUtilGetPropertyFormats, ResUtilGetPropertyFormats function [Failover Cluster], _wolf_resutilgetpropertyformats, mscs.resutilgetpropertyformats, resapi/PRESUTIL_GET_PROPERTY_FORMATS, resapi/ResUtilGetPropertyFormats
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
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilGetPropertyFormats
 - resapi/ResUtilGetPropertyFormats
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-resutils-l1-1-3.dll
 - ResUtils.dll
api_name:
 - ResUtilGetPropertyFormats
---

# ResUtilGetPropertyFormats function


## -description

Returns a property format list describing the format of a specified set of properties. The <b>PRESUTIL_GET_PROPERTY_FORMATS</b> type defines a pointer to this function.

## -parameters

### -param pPropertyTable [in]

Pointer to a <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a> property 
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

<a href="/previous-versions/windows/desktop/mscs/clusctl-cluster-get-common-property-fmts">CLUSCTL_CLUSTER_GET_COMMON_PROPERTY_FMTS</a>



<a href="/previous-versions/windows/desktop/mscs/general-utility-functions">General Utility Functions</a>



<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a>
---
UID: NC:resapi.POFFLINE_V2_ROUTINE
title: POFFLINE_V2_ROUTINE (resapi.h)
description: The POFFLINE_V2_ROUTINE callback function marks a resource as unavailable for use after cleanup processing is complete.
helpviewer_keywords: ["CLUS_RESDLL_OFFLINE_DO_NOT_UPDATE_PERSISTENT_STATE","CLUS_RESDLL_OFFLINE_DUE_TO_EMBEDDED_FAILURE","CLUS_RESDLL_OFFLINE_IGNORE_NETWORK_CONNECTIVITY","CLUS_RESDLL_OFFLINE_IGNORE_RESOURCE_STATUS","CLUS_RESDLL_OFFLINE_QUEUE_ENABLED","CLUS_RESDLL_OFFLINE_RETURNING_TO_SOURCE_NODE_BECAUSE_OF_ERROR","CLUS_RESDLL_OFFLINE_RETURN_TO_SOURCE_NODE_ON_ERROR","OfflineV2","OfflineV2 callback","OfflineV2 callback function [Failover Cluster]","POFFLINE_V2_ROUTINE","POFFLINE_V2_ROUTINE callback function [Failover Cluster]","mscs.offlinev2","resapi/OfflineV2","resapi/POFFLINE_V2_ROUTINE"]
old-location: mscs\offlinev2.htm
tech.root: MsCS
ms.assetid: 2983B328-08ED-4DA6-8DC2-79D44C710888
ms.date: 08/03/2022
ms.keywords: CLUS_RESDLL_OFFLINE_DO_NOT_UPDATE_PERSISTENT_STATE, CLUS_RESDLL_OFFLINE_DUE_TO_EMBEDDED_FAILURE, CLUS_RESDLL_OFFLINE_IGNORE_NETWORK_CONNECTIVITY, CLUS_RESDLL_OFFLINE_IGNORE_RESOURCE_STATUS, CLUS_RESDLL_OFFLINE_QUEUE_ENABLED, CLUS_RESDLL_OFFLINE_RETURNING_TO_SOURCE_NODE_BECAUSE_OF_ERROR, CLUS_RESDLL_OFFLINE_RETURN_TO_SOURCE_NODE_ON_ERROR, OfflineV2, OfflineV2 callback, OfflineV2 callback function [Failover Cluster], POFFLINE_V2_ROUTINE, POFFLINE_V2_ROUTINE callback function [Failover Cluster], mscs.offlinev2, resapi/OfflineV2, resapi/POFFLINE_V2_ROUTINE
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - POFFLINE_V2_ROUTINE
 - resapi/POFFLINE_V2_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - OfflineV2
---

# POFFLINE_V2_ROUTINE callback function


## -description

Marks a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> as unavailable for use after cleanup 
    processing is complete. The <b>POFFLINE_V2_ROUTINE</b> type defines a pointer to 
    this function.

## -parameters

### -param Resource [in]

A resource identifier for the resource to be taken offline.

### -param DestinationNodeName [in, optional]

The name of the node that is to contain the resource when the operation completes.

### -param OfflineFlags [in]

A bitmask of flags that specify settings for this operation. This parameter can be set to one or more  of the following values:



#### CLUS_RESDLL_OFFLINE_IGNORE_RESOURCE_STATUS (0x00000001)

Perform the operation even if the resource indicates that it should be locked.



#### CLUS_RESDLL_OFFLINE_RETURN_TO_SOURCE_NODE_ON_ERROR (0x00000002)

If the resource experiences an error, return it to the source node.



#### CLUS_RESDLL_OFFLINE_QUEUE_ENABLED (0x00000004)

Queue the operation if it is delayed by a resource DLL, and then retry the operation until it completes or is cancelled by the client.



#### CLUS_RESDLL_OFFLINE_RETURNING_TO_SOURCE_NODE_BECAUSE_OF_ERROR (0x00000008)

Indicate that the resource experienced an error, and is returning  to the source node.



#### CLUS_RESDLL_OFFLINE_DUE_TO_EMBEDDED_FAILURE (0x00000010)

Indicate that there was an embedded failure.



#### CLUS_RESDLL_OFFLINE_IGNORE_NETWORK_CONNECTIVITY (0x00000020)

Perform the operation even if there is network error.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.



#### CLUS_RESDLL_OFFLINE_DO_NOT_UPDATE_PERSISTENT_STATE (0x00000040)

Do not update the persistent state of the resource.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This value is not supported before Windows Server 2016.

### -param InBuffer [in, optional]

A pointer to a buffer that contains  data for the operation; otherwise <b>NULL</b> if the operation does not require data.

### -param InBufferSize [in]

The size of the <i>InBuffer</i> parameter, in bytes.

### -param Reserved [in]

Reserved.

## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The request completed successfully, and the resource is offline.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_PENDING</b></dt>
<dt>997 (0x3E5)</dt>
</dl>
</td>
<td width="60%">
The request is still pending, and a thread has been activated to process the offline request.

</td>
</tr>
</table>
 

If the operation was not successful for other reasons, 
       this function returns one of the 
       <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-entry-point-functions">Resource DLL Entry Point Functions</a>

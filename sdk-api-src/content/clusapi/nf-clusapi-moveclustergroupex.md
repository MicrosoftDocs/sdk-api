---
UID: NF:clusapi.MoveClusterGroupEx
title: MoveClusterGroupEx function (clusapi.h)
description: Extends the existing MoveClusterGroup method with the addition of flags and a buffer.
helpviewer_keywords: ["CLUSAPI_GROUP_MOVE_FAILBACK","CLUSAPI_GROUP_MOVE_HIGH_PRIORITY_START","CLUSAPI_GROUP_MOVE_IGNORE_RESOURCE_STATUS","CLUSAPI_GROUP_MOVE_QUEUE_ENABLED","CLUSAPI_GROUP_MOVE_RETURN_TO_SOURCE_NODE_ON_ERROR","MoveClusterGroupEx","MoveClusterGroupEx function [Failover Cluster]","clusapi/MoveClusterGroupEx","mscs.moveclustergroupex"]
old-location: mscs\moveclustergroupex.htm
tech.root: MsCS
ms.assetid: CE56BA9D-3527-43D3-8656-EA0BBDF48B98
ms.date: 12/05/2018
ms.keywords: CLUSAPI_GROUP_MOVE_FAILBACK, CLUSAPI_GROUP_MOVE_HIGH_PRIORITY_START, CLUSAPI_GROUP_MOVE_IGNORE_RESOURCE_STATUS, CLUSAPI_GROUP_MOVE_QUEUE_ENABLED, CLUSAPI_GROUP_MOVE_RETURN_TO_SOURCE_NODE_ON_ERROR, MoveClusterGroupEx, MoveClusterGroupEx function [Failover Cluster], clusapi/MoveClusterGroupEx, mscs.moveclustergroupex
req.header: clusapi.h
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MoveClusterGroupEx
 - clusapi/MoveClusterGroupEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - MoveClusterGroupEx
---

# MoveClusterGroupEx function


## -description

Extends the existing <a href="/windows/desktop/api/clusapi/nf-clusapi-moveclustergroup">MoveClusterGroup</a> method with the addition of flags and a buffer. The flags control the behavior of the cluster failover policy, and the input buffer enables the client to send special instructions to the resources in the group.

## -parameters

### -param hGroup [in]

The handle to a cluster group.

### -param hDestinationNode [in, optional]

The handle to a cluster node, indicating the node to which the group should be moved. This parameter is optional. If left <b>NULL</b>, the cluster will move the group to the most suitable node, according to failover policies configured for the cluster and for this particular group.

### -param dwMoveFlags [in]

A bitwise combination of the flags that influence the failover policy with respect to this move operation.



#### CLUSAPI_GROUP_MOVE_IGNORE_RESOURCE_STATUS (0x00000001)

Forces the group move even if a resource has indicated that it should be "locked" in its current state on the current node, and terminates the resource if necessary.



#### CLUSAPI_GROUP_MOVE_RETURN_TO_SOURCE_NODE_ON_ERROR (0x00000002)

If the group fails to reach its persistent state on the destination node (whether specified with <i>hDestinationNode</i> or chosen by the cluster), returns the group to the source node and brings it to its persistent state there.



#### CLUSAPI_GROUP_MOVE_QUEUE_ENABLED (0x00000004)

If a resource DLL in the group indicates that the move is not possible at this time but may be possible in the near future, queues this move in the cluster service and continues retrying, when deemed appropriate, until either the move operation completes or is cancelled by the client.



#### CLUSAPI_GROUP_MOVE_HIGH_PRIORITY_START (0x00000008)

Brings this group to its persistent state on the destination node as soon as possible without regard to implementation-specific policies that govern the ordering and/or prioritization of bringing groups to their persistent states.



#### CLUSAPI_GROUP_MOVE_FAILBACK (0x00000010)

Reserved.

### -param lpInBuffer [in, optional]

A <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a> that contains move operation instructions for specific resources within the group. The instructions are contained in property values. Resources in the group search the property list for property names that they support for move operations and then interpret the instructions in the associated property value. The properties supported by a resource in a <b>MoveClusterGroupEx</b> operation are not related to the private properties associated with a resource.

### -param cbInBufferSize [in]

The size of <i>lpInBuffer</i>, in bytes.

## -returns

<b>MoveClusterGroupEx</b> returns <b>ERROR_IO_PENDING</b> if the move command has been accepted and is in progress. <b>MoveClusterGroupEx</b> returns a nonzero error code if the move command was rejected immediately with no changes to group state. For instance, this would happen if <i>hDestinationNode</i> is not Up at the time of the move request.

## -remarks

<b>MoveClusterGroupEx</b> fails immediately with error <b>ERROR_CLUSTER_RESOURCE_LOCKED_STATUS</b> if the <b>CLUSAPI_GROUP_MOVE_IGNORE_RESOURCE_STATUS</b> flag is not set and any resource in the group is online and has indicated that it is "locked" in its current state.

After <b>MoveClusterGroupEx</b> returns <b>ERROR_IO_PENDING</b>, there are a number of possible outcomes, including:

<ul>
<li>The move operation could succeed, and the group could reach its persistent state on the target node.</li>
<li>The move operation could fail, in that the group cannot reach its persistent state on the target node. If <i>dwMoveFlags</i> does not include <b>CLUSAPI_GROUP_MOVE_RETURN_TO_SOURCE_NODE_ON_ERROR</b>, then the cluster will take appropriate action (according to configured policies) to bring the group to its persistent state, perhaps on other nodes in the cluster. If <i>dwMoveFlags</i> includes <b>CLUSAPI_GROUP_MOVE_RETURN_TO_SOURCE_NODE_ON_ERROR</b>, then the cluster will attempt to bring the group to its persistent state on the source node. If this fails, then the cluster will take appropriate action (according to configured policies) to bring the group to its persistent state, perhaps on other nodes in the cluster.</li>
<li>The move operation could be queued if a resource indicates that it cannot move immediately and the <b>CLUSAPI_GROUP_MOVE_QUEUE_ENABLED</b> flag is set.</li>
<li>The move operation could be rejected by a resource in the group, thus returning the group to its persistent state on the source node without incrementing any failure counts or triggering any failure policies. This cannot occur if the <b>CLUSAPI_GROUP_MOVE_IGNORE_RESOURCE_STATUS</b> flag is set.</li>
</ul>
For a live migration of a virtual machine, perform these steps:

<ol>
<li>In the <i>dwMoveFlags</i> parameter, set the <b>CLUSAPI_GROUP_MOVE_RETURN_TO_SOURCE_NODE_ON_ERROR</b>, <b>CLUSAPI_GROUP_MOVE_QUEUE_ENABLED</b>, and  <b>CLUSAPI_GROUP_MOVE_HIGH_PRIORITY_START</b> flags.</li>
<li>In the <i>lpInBuffer</i> parameter, add to the property list a resource type named "Virtual Machine" or "Virtual Machine Configuration" that specifies a <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_property_format">CLUSTER_PROPERTY_FORMAT</a> enumeration value of <b>CLUSPROP_FORMAT_DWORD</b> (which represents the property's data format) and a property value of <b>VmResdllContextLiveMigration</b> (from the <a href="/previous-versions/windows/desktop/api/resapi/ne-resapi-vm_resdll_context">VM_RESDLL_CONTEXT</a> enumeration of possible virtual machine actions).</li>
</ol>
<b>MoveClusterGroupEx</b> requires that the client be granted Full access in the cluster security descriptor.


#### Examples


```
#include "stdafx.h"
#include <windows.h>
#include <stdio.h>
#include <ClusAPI.h>


#define DemoResDllTypeName L"dummy"
#define DemoGroupName L"DemoGroup"


int __cdecl main( void )
{
    HCLUSTER hCluster= NULL;
    HGROUP hGroup = NULL;
    DWORD error = 0;

    hCluster = OpenCluster( NULL );
    if ( hCluster == NULL )
    {
        error = GetLastError();
        wprintf( L"Failed to open cluster: 0x%x\n", error );
        goto Cleanup;
    }

    hGroup = OpenClusterGroup( hCluster, DemoGroupName );
    if ( hGroup == NULL )
    {
        error = GetLastError();
        wprintf( L"Failed to open cluster group " DemoGroupName L": 0x%x\n", error );
        goto Cleanup;
    }


    // Move Group example
    error = MoveClusterGroupEx( hGroup,
                                NULL,
                                CLUSAPI_GROUP_MOVE_RETURN_TO_SOURCE_NODE_ON_ERROR | CLUSAPI_GROUP_MOVE_IGNORE_RESOURCE_STATUS,
                                NULL,
                                0);

    if ( error == ERROR_IO_PENDING  )
    {
        wprintf( L"Group move pending" DemoGroupName L": 0x%x\n", error );
        error = ERROR_SUCCESS;
    }
    else if ( error != ERROR_SUCCESS)
    {
        wprintf( L"Failed to move group" DemoGroupName L": 0x%x\n", error );
    }
    else 
    {
        wprintf( L"Group move completed" DemoGroupName L": 0x%x\n");
    }

Cleanup:

    if ( hGroup != NULL )
    {
        CloseClusterGroup( hGroup );
        hGroup = NULL;
    }
    if ( hCluster != NULL )
    {
        CloseCluster( hCluster );
        hCluster = NULL;
    }

    return (int)error;
}

```
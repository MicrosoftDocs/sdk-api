---
UID: NF:clusapi.OfflineClusterGroupEx
title: OfflineClusterGroupEx function (clusapi.h)
description: Extends the OfflineClusterGroup method.
helpviewer_keywords: ["OfflineClusterGroupEx","OfflineClusterGroupEx function [Failover Cluster]","clusapi/OfflineClusterGroupEx","mscs.offlineclustergroupex"]
old-location: mscs\offlineclustergroupex.htm
tech.root: MsCS
ms.assetid: ED22150C-7149-4CED-9C9B-356BCEEBF11F
ms.date: 12/05/2018
ms.keywords: OfflineClusterGroupEx, OfflineClusterGroupEx function [Failover Cluster], clusapi/OfflineClusterGroupEx, mscs.offlineclustergroupex
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
 - OfflineClusterGroupEx
 - clusapi/OfflineClusterGroupEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - OfflineClusterGroupEx
---

# OfflineClusterGroupEx function


## -description

Extends the <a href="/windows/desktop/api/clusapi/nf-clusapi-offlineclustergroup">OfflineClusterGroup</a> method. 
    The client can use the flags to control failover policies of the group and the input buffer to send specific 
    instructions for the offline operation to the resources in the target group. For instance, the input buffer can be 
    used to instruct a virtual machine to go offline by saving its state as opposed to shutting down.

## -parameters

### -param hGroup [in]

The handle to a cluster group.

### -param dwOfflineFlags [in]

Flags that influence the offline policy. Along with 0x0, the following is an acceptable value: 
      <b>CLUSAPI_GROUP_OFFLINE_IGNORE_RESOURCE_LOCKED_STATUS</b> (0x00000001): disregard if a 
      resource has indicated that it should be “locked” in its current state.

### -param lpInBuffer

Contains instructions for the offline operation that are targeted at specific resources within the group. 
      <i>lpInBuffer</i> is formatted as a property list, which means that the instructions are 
      contained in property values. Resources in the group search the property list for property names that they 
      support for offline operations and then interpret the instructions in the associated property value. Note that 
      the properties supported by a resource in an 
      <b>OfflineClusterGroupEx</b> operation are not 
      related to the private properties associated with a resource.

### -param cbInBufferSize [in]

The size of <i>lpInBuffer</i>, in bytes.

## -returns

<b>OfflineClusterGroupEx</b> returns 
      <b>ERROR_IO_PENDING</b> if the offline command has been accepted and is in progress. 
      <b>OfflineClusterGroupEx</b> returns a nonzero error 
      code if the offline command was rejected immediately with no changes to group state.

## -remarks

<b>OfflineClusterGroupEx</b> fails immediately with 
    error <b>ERROR_CLUSTER_RESOURCE_LOCKED_STATUS</b> if the 
    <b>CLUSAPI_OFFLINE_GROUP_IGNORE_RESOURCE_LOCKED_STATUS</b> flag is not set and any resource in 
    the group has indicated that it is “locked” in its current state.

Similar to <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-moveclustergroupex">MoveClusterGroupEx</a>, if 
    <b>OfflineClusterGroupEx</b> returns 
    <b>ERROR_IO_PENDING</b>, then the cluster service will attempt to bring the group to the 
    offline state.

<b>OfflineClusterGroupEx</b> requires that the client 
    be granted Full access in the cluster security descriptor.


#### Examples


```
#include "stdafx.h"
#include <windows.h>
#include <stdio.h>
#include <ClusAPI.h>


#define DemoResDllTypeName L"dummy"
#define DemoGroupName L"DemoGroup"


BOOL WaitForGroupToGoOffline(__in HGROUP hGroup)
{
    for(;;)
    {
        CLUSTER_GROUP_STATE state = GetClusterGroupState( hGroup, NULL, NULL );
        if( state == ClusterGroupFailed || state == ClusterGroupPartialOnline || state == ClusterGroupOnline)
        {
            return false;
        }
        else if ( state == ClusterGroupOffline )
        {
            return true;
        }

        Sleep(100);
    }
}

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

    // Offlining Group example
    error = OfflineClusterGroupEx(hGroup, CLUSAPI_GROUP_OFFLINE_IGNORE_RESOURCE_STATUS, NULL, 0);
    if ( error == ERROR_IO_PENDING  )
    {
        if (WaitForGroupToGoOffline(hGroup))
        {
            error = ERROR_SUCCESS;
        }
    }
    if ( error )
    {
        wprintf( L"Failed to offline the group" DemoGroupName L": 0x%x\n", error );
        goto Cleanup;
    }
    else
    {
        wprintf( L"Offlined the group" DemoGroupName);
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
---
UID: NF:clusapi.OfflineClusterResourceEx
title: OfflineClusterResourceEx function (clusapi.h)
description: Extends the OfflineClusterResource method.
helpviewer_keywords: ["CLUSAPI_RESOURCE_OFFLINE_FORCE_WITH_TERMINATION","CLUSAPI_RESOURCE_OFFLINE_IGNORE_RESOURCE_STATUS","CLUSAPI_RESOURCE_OFFLINE_REASON_BEING_DELETED","CLUSAPI_RESOURCE_OFFLINE_REASON_BEING_RESTARTED","CLUSAPI_RESOURCE_OFFLINE_REASON_MOVING","CLUSAPI_RESOURCE_OFFLINE_REASON_NONE","CLUSAPI_RESOURCE_OFFLINE_REASON_PREEMPTED","CLUSAPI_RESOURCE_OFFLINE_REASON_SHUTTING_DOWN","CLUSAPI_RESOURCE_OFFLINE_REASON_UNKNOWN","CLUSAPI_RESOURCE_OFFLINE_REASON_USER_REQUESTED","OfflineClusterResourceEx","OfflineClusterResourceEx function [Failover Cluster]","clusapi/OfflineClusterResourceEx","mscs.offlineclusterresourceex"]
old-location: mscs\offlineclusterresourceex.htm
tech.root: MsCS
ms.assetid: 8AE70F5F-349B-40D1-830B-A135D4364B83
ms.date: 12/05/2018
ms.keywords: CLUSAPI_RESOURCE_OFFLINE_FORCE_WITH_TERMINATION, CLUSAPI_RESOURCE_OFFLINE_IGNORE_RESOURCE_STATUS, CLUSAPI_RESOURCE_OFFLINE_REASON_BEING_DELETED, CLUSAPI_RESOURCE_OFFLINE_REASON_BEING_RESTARTED, CLUSAPI_RESOURCE_OFFLINE_REASON_MOVING, CLUSAPI_RESOURCE_OFFLINE_REASON_NONE, CLUSAPI_RESOURCE_OFFLINE_REASON_PREEMPTED, CLUSAPI_RESOURCE_OFFLINE_REASON_SHUTTING_DOWN, CLUSAPI_RESOURCE_OFFLINE_REASON_UNKNOWN, CLUSAPI_RESOURCE_OFFLINE_REASON_USER_REQUESTED, OfflineClusterResourceEx, OfflineClusterResourceEx function [Failover Cluster], clusapi/OfflineClusterResourceEx, mscs.offlineclusterresourceex
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
 - OfflineClusterResourceEx
 - clusapi/OfflineClusterResourceEx
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
 - OfflineClusterResourceEx
---

# OfflineClusterResourceEx function


## -description

Extends the <a href="/windows/desktop/api/clusapi/nf-clusapi-offlineclusterresource">OfflineClusterResource</a> 
    method. The client can use the flags to control policies of the resource and the input buffer to send specific 
    instructions for the offline operation to the resource. For instance, the input buffer can be used to instruct a 
    VM to go offline by saving its state as opposed to shutting down.

## -parameters

### -param hResource [in]

The handle to a cluster resource.

### -param dwOfflineFlags [in]

Flags that influence the offline policy.


This parameter can be set to one or more of the following values:





#### CLUSAPI_RESOURCE_OFFLINE_IGNORE_RESOURCE_STATUS (0x00000001)

Ignore the status of the resource if the resource is locked.



#### CLUSAPI_RESOURCE_OFFLINE_FORCE_WITH_TERMINATION (0x00000002)

The resource is to be marked as unavailable and shut down without waiting for the  cleanup process to 
        complete.



#### CLUSAPI_RESOURCE_OFFLINE_REASON_NONE (0x00000000)

No flags are specified.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.



#### CLUSAPI_RESOURCE_OFFLINE_REASON_UNKNOWN (0x00000001)

The reason is unknown.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.



#### CLUSAPI_RESOURCE_OFFLINE_REASON_MOVING (0x00000002)

The resource is being moved to another node.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.



#### CLUSAPI_RESOURCE_OFFLINE_REASON_USER_REQUESTED (0x00000004)

There was a user request to bring the resource offline.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.



#### CLUSAPI_RESOURCE_OFFLINE_REASON_BEING_DELETED (0x00000008)

The resource is being deleted.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.



#### CLUSAPI_RESOURCE_OFFLINE_REASON_BEING_RESTARTED (0x00000010)

The resource is being restarted.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.



#### CLUSAPI_RESOURCE_OFFLINE_REASON_PREEMPTED (0x00000020)

The resource had a preemptive failure.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.



#### CLUSAPI_RESOURCE_OFFLINE_REASON_SHUTTING_DOWN (0x00000040)

The resource is shutting down.

<b>Windows Server 2012:  </b>This value is not supported before Windows Server 2012 R2.

### -param lpInBuffer [in]

Contains instructions for the offline operation that are targeted at the specific resource. 
      <i>lpInBuffer</i> is formatted as a property list, which means that the instructions are 
      contained in property values. The resource DLL searches the property list for property names that it supports 
      for offline operations and then interprets the instructions in the associated property value. Note that the 
      properties supported by a resource in an 
      <b>OfflineClusterResourceEx</b> operation are not 
      related to the private properties associated with a resource.

### -param cbInBufferSize [in]

The size of <i>lpInBuffer</i>, in bytes.

## -returns

<b>OfflineClusterResourceEx</b> returns 
      <b>ERROR_IO_PENDING</b> if the offline command has been accepted and is in progress. 
      <b>OfflineClusterResourceEx</b> returns a nonzero 
      error code if the offline command was rejected immediately with no changes to resource state.

## -remarks

<b>OfflineClusterResourceEx</b> fails immediately 
    with error <b>ERROR_CLUSTER_RESOURCE_LOCKED_STATUS</b> if the 
    <b>CLUSAPI_RESOURCE_OFFLINE_IGNORE_RESOURCE_LOCKED_STATUS</b> flag is not set and the resource 
    has indicated that it is “locked” in its current state.

Similar to <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-moveclustergroupex">MoveClusterGroupEx</a>, if 
    <b>OfflineClusterResourceEx</b> returns 
    <b>ERROR_IO_PENDING</b>, then the cluster service will attempt to bring the resource to the 
    offline state.

<b>OfflineClusterResourceEx</b> requires that the 
    client be granted Full access in the cluster security descriptor.


#### Examples


```
#include "stdafx.h"
#include <windows.h>
#include <stdio.h>
#include <ClusAPI.h>


#define DemoResDllTypeName L"dummy"
#define DemoResourceName L"DemoResource"


BOOL WaitForResourceToGoOffline(__in HRESOURCE hResource)
{
    for(;;)
    {
        CLUSTER_RESOURCE_STATE state = GetClusterResourceState( hResource, NULL, 0, NULL, 0 );
        if( state == ClusterResourceOnline || state == ClusterResourceFailed)
        {
            return false;
        }
        else if ( state == ClusterResourceOffline )
        {
            return true;
        }

        Sleep(100);
    }
}

int __cdecl main( void )
{
    HCLUSTER hCluster= NULL;
    HRESOURCE hResource = NULL;
    DWORD error = 0;
    
    hCluster = OpenCluster( NULL );
    if ( hCluster == NULL )
    {
        error = GetLastError();
        wprintf( L"Failed to open cluster: 0x%x\n", error );
        goto Cleanup;
    }

    hResource = OpenClusterResource( hCluster, DemoResourceName );
    if ( hResource == NULL )
    {
        error = GetLastError();
        wprintf( L"Failed to open cluster resource " DemoResourceName L": 0x%x\n", error );
        goto Cleanup;
    }

    // Offlining Resource example
    error = OfflineClusterResourceEx(hResource, CLUSAPI_RESOURCE_OFFLINE_IGNORE_RESOURCE_STATUS, NULL, 0);
    if ( error == ERROR_IO_PENDING  )
    {
        if (WaitForResourceToGoOffline(hResource))
        {
            error = ERROR_SUCCESS;
        }
    }
    if ( error )
    {
        wprintf( L"Failed to offline the resource" DemoResourceName L": 0x%x\n", error );
        goto Cleanup;
    }
    else
    {
        wprintf( L"Offlined the resource" DemoResourceName);
    }


Cleanup:

    if ( hResource != NULL )
    {
        CloseClusterResource( hResource );
        hResource = NULL;
    }
    if ( hCluster != NULL )
    {
        CloseCluster( hCluster );
        hCluster = NULL;
    }

    return (int)error;
}
```
---
UID: NF:clusapi.CancelClusterGroupOperation
title: CancelClusterGroupOperation function (clusapi.h)
description: Enables a client to cancel a MoveClusterGroup or MoveClusterGroupEx operation that is pending for a group. The group is then returned to its persistent state.
helpviewer_keywords: ["CancelClusterGroupOperation","CancelClusterGroupOperation function [Failover Cluster]","clusapi/CancelClusterGroupOperation","mscs.cancelclustergroupoperation"]
old-location: mscs\cancelclustergroupoperation.htm
tech.root: MsCS
ms.assetid: F7710CD6-2B02-48A5-B089-7F174B18463C
ms.date: 12/05/2018
ms.keywords: CancelClusterGroupOperation, CancelClusterGroupOperation function [Failover Cluster], clusapi/CancelClusterGroupOperation, mscs.cancelclustergroupoperation
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
 - CancelClusterGroupOperation
 - clusapi/CancelClusterGroupOperation
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
 - CancelClusterGroupOperation
---

# CancelClusterGroupOperation function


## -description

Enables a client to cancel a 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-moveclustergroup">MoveClusterGroup</a> or 
    <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-moveclustergroupex">MoveClusterGroupEx</a> operation that is pending for a 
    group. The group is then returned to its persistent state.

## -parameters

### -param hGroup [in]

The handle to a cluster group.

### -param dwCancelFlags_RESERVED [in]

This parameter is reserved for future use and must be set to zero.

## -returns

<b>CancelClusterGroupOperation</b> returns 
      <b>ERROR_SUCCESS</b> if the move operation on the group was successfully cancelled.

<b>CancelClusterGroupOperation</b> returns 
      <b>ERROR_IO_PENDING</b> if the cancellation of the move operation is now in progress.

<b>CancelClusterGroupOperation</b> returns a 
      different nonzero error code if there was a failure issuing the cancellation for the move group operation on the 
      designated group.

## -remarks

<b>CancelClusterGroupOperation</b> attempts to 
    cancel a pending move operation on a cluster group that was issued through a 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-moveclustergroup">MoveClusterGroup</a> or 
    <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-moveclustergroupex">MoveClusterGroupEx</a> call that returned 
    <b>ERROR_IO_PENDING</b> and is still in progress. The call attempts to cancel the pending move 
    operation and bring the group to its persistent state.


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


    // Cancel Move Group example
    error = MoveClusterGroupEx( hGroup,
                                NULL,
                                CLUSAPI_GROUP_MOVE_RETURN_TO_SOURCE_NODE_ON_ERROR | CLUSAPI_GROUP_MOVE_IGNORE_RESOURCE_STATUS,
                                NULL,
                                0);

    if ( error == ERROR_IO_PENDING  )
    {
        wprintf( L"Group move pending" DemoGroupName L": 0x%x\n", error );
        error = ERROR_SUCCESS;

        // Issuing cancel to the move operation
        error = CancelClusterGroupOperation(hGroup, 0);
        if ( error == ERROR_IO_PENDING  || error == ERROR_SUCCESS )
        {
            // the cancel was registered successfully
            wprintf( L"Cancel issued for move operation for the group " DemoGroupName L"\n" );
        }
        else
        {
            wprintf( L"Failed to Cancel move operation for the group " DemoGroupName L": 0x%x\n" );
        }
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
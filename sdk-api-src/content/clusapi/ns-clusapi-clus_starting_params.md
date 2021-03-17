---
UID: NS:clusapi.CLUS_STARTING_PARAMS
title: CLUS_STARTING_PARAMS (clusapi.h)
description: Indicates whether a node's attempt to start the Cluster service represents an attempt to form or join a cluster, and whether the node has attempted to start this version of the Cluster service before.
helpviewer_keywords: ["*PCLUS_STARTING_PARAMS","CLUS_STARTING_PARAMS","CLUS_STARTING_PARAMS structure [Failover Cluster]","FALSE","PCLUS_STARTING_PARAMS","PCLUS_STARTING_PARAMS structure pointer [Failover Cluster]","TRUE","_wolf_clus_starting_params","clusapi/CLUS_STARTING_PARAMS","clusapi/PCLUS_STARTING_PARAMS","mscs.clus_starting_params"]
old-location: mscs\clus_starting_params.htm
tech.root: MsCS
ms.assetid: 255c68ff-0ca0-4718-b7fe-c689c93d0203
ms.date: 12/05/2018
ms.keywords: '*PCLUS_STARTING_PARAMS, CLUS_STARTING_PARAMS, CLUS_STARTING_PARAMS structure [Failover Cluster], FALSE, PCLUS_STARTING_PARAMS, PCLUS_STARTING_PARAMS structure pointer [Failover Cluster], TRUE, _wolf_clus_starting_params, clusapi/CLUS_STARTING_PARAMS, clusapi/PCLUS_STARTING_PARAMS, mscs.clus_starting_params'
req.header: clusapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CLUS_STARTING_PARAMS, *PCLUS_STARTING_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_STARTING_PARAMS
 - clusapi/CLUS_STARTING_PARAMS
 - PCLUS_STARTING_PARAMS
 - clusapi/PCLUS_STARTING_PARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUS_STARTING_PARAMS
---

# CLUS_STARTING_PARAMS structure


## -description

Indicates whether a  <a href="/previous-versions/windows/desktop/mscs/nodes">node's</a> attempt to start the  <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a> represents an attempt to form or join a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>, and whether the node has attempted to start this version of the Cluster service before.  <a href="/previous-versions/windows/desktop/mscs/resource-dlls">Resource DLLs</a> receive the CLUS_STARTING_PARAMS structure with the  <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-starting-phase1">CLUSCTL_RESOURCE_TYPE_STARTING_PHASE1</a> and  <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-starting-phase2">CLUSCTL_RESOURCE_TYPE_STARTING_PHASE2</a> control codes.

## -struct-fields

### -field dwSize

Byte size of the structure.

### -field bForm

Indicates whether this particular start of the Cluster service represents a form or a join operation.



#### TRUE

The node starting the Cluster service is attempting to form a cluster. No other nodes are currently active.



#### FALSE

The node starting the Cluster service is attempting to join an existing cluster. At least one other node is currently active.

### -field bFirst

Indicates whether this version of the Cluster service has ever started on the node.



#### TRUE

The node is starting a version of the Cluster service for the first time.



#### FALSE

The node has started this version of the Cluster service previously.

## -remarks

The  <b>CLUS_STARTING_PARAMS</b> structure allows resource DLLs to respond to the CLUSCTL_RESOURCE_TYPE_STARTING_PHASE1 and CLUSCTL_RESOURCE_TYPE_STARTING_PHASE2 control codes based on the circumstances of the start. For example, a DLL might perform special initialization steps when the cluster forms, and perform another set of operations in response to joins.


#### Examples

The following example illustrates an abbreviated implementation of  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-presource_type_control_routine">ResourceTypeControl</a>. For more information, see  <a href="/previous-versions/windows/desktop/mscs/implementing-resourcetypecontrol">Implementing ResourceTypeControl</a>.


```cpp
const LPWSTR g_MY_RESOURCE_TYPE_NAME[] =
{
    L"MyType_0",
    L"MyType_1",
    L"MyType_2",
    L"MyType_3"
};

DWORD WINAPI MyDllResourceTypeControl(
    IN LPCWSTR ResourceTypeName,
    IN DWORD ControlCode,
    IN PVOID InBuffer,
    IN DWORD InBufferSize,
    OUT PVOID OutBuffer,
    IN DWORD OutBufferSize,
    OUT LPDWORD BytesReturned
)
{
    DWORD status;
    PCLUS_STARTING_PARAMS pStart;

    switch ( ControlCode )
    {
        case CLUSCTL_RESOURCE_TYPE_STARTING_PHASE1:

            if( lstrcmpi( ResourceTypeName, g_MY_RESOURCE_TYPE_NAME[2] ) == 0 )
            {
                pStart = (PCLUS_STARTING_PARAMS) InBuffer;
                if( ( pStart->bForm == TRUE ) && 
                    ( pStart->bFirst == FALSE ) )
                {
                //  Hypothetical initialization code for resource type "MyType_2"
                //  Fires only when the cluster forms, but not for first-time launches of the Cluster service.
                }
            }
            else
            {
                status = ERROR_INVALID_FUNCTION;
            }

            break;

        case CLUSCTL_RESOURCE_TYPE_STARTING_PHASE2:

            pStart = (PCLUS_STARTING_PARAMS) InBuffer;
            if( pStart->bFirst == TRUE )
            {
            //  Hypothetical verification code for all resource types supported by the DLL
            //  Fires for first-time launches of the Cluster service
            }
            else
            {
                status = ERROR_INVALID_FUNCTION;
            }

            break;

    //  case ( Other control codes )....
    //      ...
    //      break;

        default:
            status = ERROR_INVALID_FUNCTION;
            break;

    }
    // end switch

    return( status );

}
// MyDllResourceTypeControl

```

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-starting-phase1">CLUSCTL_RESOURCE_TYPE_STARTING_PHASE1</a>



<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-starting-phase2">CLUSCTL_RESOURCE_TYPE_STARTING_PHASE2</a>
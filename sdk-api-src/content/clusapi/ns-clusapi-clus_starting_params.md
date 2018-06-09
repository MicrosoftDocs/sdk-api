---
UID: NS:clusapi.CLUS_STARTING_PARAMS
title: CLUS_STARTING_PARAMS
author: windows-sdk-content
description: Indicates whether a node's attempt to start the Cluster service represents an attempt to form or join a cluster, and whether the node has attempted to start this version of the Cluster service before.
old-location: mscs\clus_starting_params.htm
old-project: MsCS
ms.assetid: 255c68ff-0ca0-4718-b7fe-c689c93d0203
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: "*PCLUS_STARTING_PARAMS, CLUS_STARTING_PARAMS, CLUS_STARTING_PARAMS structure [Failover Cluster], FALSE, PCLUS_STARTING_PARAMS, PCLUS_STARTING_PARAMS structure pointer [Failover Cluster], TRUE, _wolf_clus_starting_params, clusapi/CLUS_STARTING_PARAMS, clusapi/PCLUS_STARTING_PARAMS, mscs.clus_starting_params"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: CLUS_STARTING_PARAMS, *PCLUS_STARTING_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUS_STARTING_PARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CLUS_STARTING_PARAMS structure


## -description


Indicates whether a  <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node's</a> attempt to start the  <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> represents an attempt to form or join a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>, and whether the node has attempted to start this version of the Cluster service before.  <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">Resource DLLs</a> receive the CLUS_STARTING_PARAMS structure with the  <a href="https://msdn.microsoft.com/3a66a48c-ddd3-464c-8254-bf842dd174b2">CLUSCTL_RESOURCE_TYPE_STARTING_PHASE1</a> and  <a href="https://msdn.microsoft.com/5187e72c-2838-487b-a897-0b4f99f6f9df">CLUSCTL_RESOURCE_TYPE_STARTING_PHASE2</a> control codes.


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

The following example illustrates an abbreviated implementation of  <a href="https://msdn.microsoft.com/dc4a6e6e-f968-4502-88d0-dc692341528d">ResourceTypeControl</a>. For more information, see  <a href="https://msdn.microsoft.com/23d16976-1491-43d7-9dea-9cd8ae8086cb">Implementing ResourceTypeControl</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>const LPWSTR g_MY_RESOURCE_TYPE_NAME[] =
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
                if( ( pStart-&gt;bForm == TRUE ) &amp;&amp; 
                    ( pStart-&gt;bFirst == FALSE ) )
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
            if( pStart-&gt;bFirst == TRUE )
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3a66a48c-ddd3-464c-8254-bf842dd174b2">CLUSCTL_RESOURCE_TYPE_STARTING_PHASE1</a>



<a href="https://msdn.microsoft.com/5187e72c-2838-487b-a897-0b4f99f6f9df">CLUSCTL_RESOURCE_TYPE_STARTING_PHASE2</a>
 

 


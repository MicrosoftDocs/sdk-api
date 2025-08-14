---
UID: NF:resapi.ResUtilEnumResources
title: ResUtilEnumResources function (resapi.h)
description: Enumerates all of the resources in the local cluster and initiates a user-defined operation for each resource. The PRESUTIL_ENUM_RESOURCES type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_ENUM_RESOURCES","PRESUTIL_ENUM_RESOURCES function [Failover Cluster]","ResUtilEnumResources","ResUtilEnumResources function [Failover Cluster]","_wolf_resutilenumresources","mscs.resutilenumresources","resapi/PRESUTIL_ENUM_RESOURCES","resapi/ResUtilEnumResources"]
old-location: mscs\resutilenumresources.htm
tech.root: MsCS
ms.assetid: 109fefb7-a5fc-44d2-80c0-9a08ce8d91bf
ms.date: 12/05/2018
ms.keywords: PRESUTIL_ENUM_RESOURCES, PRESUTIL_ENUM_RESOURCES function [Failover Cluster], ResUtilEnumResources, ResUtilEnumResources function [Failover Cluster], _wolf_resutilenumresources, mscs.resutilenumresources, resapi/PRESUTIL_ENUM_RESOURCES, resapi/ResUtilEnumResources
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
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilEnumResources
 - resapi/ResUtilEnumResources
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
 - ResUtilEnumResources
---

# ResUtilEnumResources function


## -description

Enumerates all of the <a href="/previous-versions/windows/desktop/mscs/resources">resources</a> in the local 
    <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> and initiates a user-defined operation for each 
    resource. The <b>PRESUTIL_ENUM_RESOURCES</b> type defines a pointer to this function.

## -parameters

### -param hSelf [in]

Optional handle to a cluster resource. The callback function is not invoked for a resource identified by 
       <i>hSelf</i>.

### -param lpszResTypeName [in]

Optional pointer to a name of a <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a> that 
       narrows the scope of resources to enumerate. If <i>lpszResTypeName</i> is specified, only 
       resources of the specified type are enumerated.

### -param pResCallBack [in]

Pointer to a user-defined function which will be called for each enumerated resource. This function must 
       conform to the definition of the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-lpresource_callback">ResourceCallback</a> 
       callback function (note that parameter names are not part of the definition; they have been added here for 
       clarity):


``` syntax
DWORD (*LPRESOURCE_CALLBACK)( 
  HRESOURCE hSelf, 
  HRESOURCE hEnum, 
  PVOID pParameter 
);
```


### -param pParameter [in]

A generic buffer that allows you to pass any kind of data to the callback function. 
       <b>ResUtilEnumResources</b> does not use this 
       parameter at all, it merely passes the pointer to the callback function. Whether you can pass 
       <b>NULL</b> for the parameter depends on how the callback function is implemented.

## -returns

If the operation succeeds or if <i>pResCallBack</i> returns 
       <b>ERROR_NO_MORE_ITEMS</b>, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function immediately halts the enumeration and returns the value returned by the 
       callback function.

## -remarks

<b>ResUtilEnumResources</b> is a convenient and 
     easy-to-use alternative to the 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceenum">ClusterResourceEnum</a> function.

<b>ResUtilEnumResources</b> must be run on a cluster 
     node because it only connects to the local cluster. The 
     <a href="/windows/desktop/api/resapi/nf-resapi-resutilenumresourcesex">ResUtilEnumResourcesEx</a> function allows you to 
     specify a remote cluster.

The following example uses 
      <b>ResUtilEnumResources</b> to list the names and 
      states of all resources in the cluster.


```cpp
//////////////////////////////////////////////////////////////////////
//  ClusDocEx_EnumDemo.cpp
//
//  Uses the ResUtilEnumResources function to list the names and 
//  states of all cluster resources.
//
//  To compile and run this example you will need two other examples 
//  from the documentation:  ClusDocEx.h (see "ClusDocEx.h") and 
//  ClusDocEx_GetControlCodeOutput.cpp (see "Getting Information with 
//  Control Codes").
// 
//////////////////////////////////////////////////////////////////////
#include "ClusDocEx.h"
#include "ClusDocEx_GetControlCodeOutput.cpp"

DWORD
MyCallbackFunction(
    HRESOURCE hSelf,
    HRESOURCE hCurrentEnum,
    PVOID pData );

LPRESOURCE_CALLBACK g_pMyCallbackFunction = &MyCallbackFunction;

int main( void )
{
    wprintf( L"\n\nResource (State)\n----------------\n" );
    DWORD dwResult = ResUtilEnumResources( 
                         NULL, 
                         NULL, 
                         g_pMyCallbackFunction, 
                         NULL );
    if( dwResult != ERROR_SUCCESS )
    {
        ClusDocEx_DebugPrint( L"ResUtilEnumResources returned an error.", dwResult );
        return 1;
    }
    else
        return 0;
}

DWORD
MyCallbackFunction(
    HRESOURCE hSelf,
    HRESOURCE hCurrentEnum,
    PVOID pData )
{
    DWORD dwResult           = ERROR_SUCCESS,
          cbNameSize         = 0, 
          dwState            = 0;

    WCHAR* pszState    = NULL;
    WCHAR* pszEnumName = ClusDocEx_ResGetControlCodeOutput(
                            hCurrentEnum,
                            NULL,
                            CLUSCTL_RESOURCE_GET_NAME,
                            &cbNameSize );
    if( pszEnumName == NULL )
    {
        dwResult = GetLastError();
        goto EndFunc;
    }

    dwState = GetClusterResourceState(
                  hCurrentEnum,
                  NULL,
                  NULL,
                  NULL,
                  NULL );
    switch( dwState )
    {
    case ClusterResourceOnline:
        pszState = L"Online";
        break;
    case ClusterResourceOffline:
        pszState = L"Offline";
        break;
    case ClusterResourcePending:
        pszState = L"Pending";
        break;
    case ClusterResourceOnlinePending:
        pszState = L"OnlinePending";
        break;
    case ClusterResourceOfflinePending:
        pszState = L"OfflinePending";
        break;
    case ClusterResourceFailed:
        pszState = L"Failed";
        break;
    case ClusterResourceInitializing:
        pszState = L"Initializing";
        break;
    default:
        pszState = L"Unknown";
        break;
    }
    wprintf( L"%ls (%ls)\n", pszEnumName, pszState );

EndFunc:
    LocalFree( pszEnumName );
    return dwResult;
}

```

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusteropenenum">ClusterOpenEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="/previous-versions/windows/desktop/mscs/resource-utility-functions">Resource Utility Functions</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-lpresource_callback">ResourceCallback</a>

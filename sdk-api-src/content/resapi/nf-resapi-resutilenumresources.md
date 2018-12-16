---
UID: NF:resapi.ResUtilEnumResources
title: ResUtilEnumResources function
author: windows-sdk-content
description: Enumerates all of the resources in the local cluster and initiates a user-defined operation for each resource. The PRESUTIL_ENUM_RESOURCES type defines a pointer to this function.
old-location: mscs\resutilenumresources.htm
tech.root: mscs
ms.assetid: 109fefb7-a5fc-44d2-80c0-9a08ce8d91bf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PRESUTIL_ENUM_RESOURCES, PRESUTIL_ENUM_RESOURCES function [Failover Cluster], ResUtilEnumResources, ResUtilEnumResources function [Failover Cluster], _wolf_resutilenumresources, mscs.resutilenumresources, resapi/PRESUTIL_ENUM_RESOURCES, resapi/ResUtilEnumResources
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilEnumResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilEnumResources function


## -description


Enumerates all of the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> in the local 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a> and initiates a user-defined operation for each 
    resource. The <b>PRESUTIL_ENUM_RESOURCES</b> type defines a pointer to this function.


## -parameters




### -param hSelf [in]

Optional handle to a cluster resource. The callback function is not invoked for a resource identified by 
       <i>hSelf</i>.


### -param lpszResTypeName [in]

Optional pointer to a name of a <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a> that 
       narrows the scope of resources to enumerate. If <i>lpszResTypeName</i> is specified, only 
       resources of the specified type are enumerated.


### -param pResCallBack [in]

Pointer to a user-defined function which will be called for each enumerated resource. This function must 
       conform to the definition of the <a href="https://msdn.microsoft.com/1e36be6d-d869-4af9-b22a-401638701bd2">ResourceCallback</a> 
       callback function (note that parameter names are not part of the definition; they have been added here for 
       clarity):

<pre class="syntax" xml:space="preserve"><code>DWORD (*LPRESOURCE_CALLBACK)( 
  HRESOURCE hSelf, 
  HRESOURCE hEnum, 
  PVOID pParameter 
);</code></pre>

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
     <a href="https://msdn.microsoft.com/73627594-90df-496d-8120-b24c34f13fb5">ClusterResourceEnum</a> function.

<b>ResUtilEnumResources</b> must be run on a cluster 
     node because it only connects to the local cluster. The 
     <a href="https://msdn.microsoft.com/e9f2e203-bbfb-4b27-b9ca-ab6b6ea1e60f">ResUtilEnumResourcesEx</a> function allows you to 
     specify a remote cluster.

The following example uses 
      <b>ResUtilEnumResources</b> to list the names and 
      states of all resources in the cluster.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//////////////////////////////////////////////////////////////////////
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

LPRESOURCE_CALLBACK g_pMyCallbackFunction = &amp;MyCallbackFunction;

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
                            &amp;cbNameSize );
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/42eb7c1b-6bd6-4997-b33e-ed16470c8475">Resource Utility Functions</a>



<a href="https://msdn.microsoft.com/1e36be6d-d869-4af9-b22a-401638701bd2">ResourceCallback</a>
 

 


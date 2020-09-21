---
UID: NF:resapi.ResUtilGetResourceDependentIPAddressProps
title: ResUtilGetResourceDependentIPAddressProps function (resapi.h)
description: Retrieves the private properties of the first IP Address dependency found for a specified resource. The PRESUTIL_GET_RESOURCE_DEPENDENTIP_ADDRESS_PROPS type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_RESOURCE_DEPENDENTIP_ADDRESS_PROPS","PRESUTIL_GET_RESOURCE_DEPENDENTIP_ADDRESS_PROPS function [Failover Cluster]","ResUtilGetResourceDependentIPAddressProps","ResUtilGetResourceDependentIPAddressProps function [Failover Cluster]","_wolf_resutilgetresourcedependentipaddressprops","mscs.resutilgetresourcedependentipaddressprops","resapi/PRESUTIL_GET_RESOURCE_DEPENDENTIP_ADDRESS_PROPS","resapi/ResUtilGetResourceDependentIPAddressProps"]
old-location: mscs\resutilgetresourcedependentipaddressprops.htm
tech.root: MsCS
ms.assetid: 283b0086-1dbf-45dc-9651-93af9a9ff6d0
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_RESOURCE_DEPENDENTIP_ADDRESS_PROPS, PRESUTIL_GET_RESOURCE_DEPENDENTIP_ADDRESS_PROPS function [Failover Cluster], ResUtilGetResourceDependentIPAddressProps, ResUtilGetResourceDependentIPAddressProps function [Failover Cluster], _wolf_resutilgetresourcedependentipaddressprops, mscs.resutilgetresourcedependentipaddressprops, resapi/PRESUTIL_GET_RESOURCE_DEPENDENTIP_ADDRESS_PROPS, resapi/ResUtilGetResourceDependentIPAddressProps
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
 - ResUtilGetResourceDependentIPAddressProps
 - resapi/ResUtilGetResourceDependentIPAddressProps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilGetResourceDependentIPAddressProps
---

# ResUtilGetResourceDependentIPAddressProps function


## -description

Retrieves the <a href="/previous-versions/windows/desktop/mscs/private-properties">private properties</a> of the 
    first IP Address <a href="/previous-versions/windows/desktop/mscs/resource-dependencies">dependency</a> found for a specified 
    <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. The <b>PRESUTIL_GET_RESOURCE_DEPENDENTIP_ADDRESS_PROPS</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle to the resource to query for dependencies.

### -param pszAddress [out]

Output buffer for returning the value of the 
      <a href="/previous-versions/windows/desktop/mscs/ip-addresses-address">Address</a> private property.

### -param pcchAddress [in, out]

On input, specifies the size of the <i>pszAddress</i> buffer as a count of 
      <b>WCHAR</b>s. On output, specifies the size of the resulting data as a count of 
      <b>WCHAR</b>s that includes the terminating <b>NULL</b>.

### -param pszSubnetMask [out]

Output buffer for returning the value of the 
      <a href="/previous-versions/windows/desktop/mscs/ip-addresses-subnetmask">SubnetMask</a> private property.

### -param pcchSubnetMask [in, out]

On input, specifies the size of the <i>pszSubnetMask</i> buffer as a count of 
      <b>WCHAR</b>s. On output, specifies the size of the resulting data as a count of 
      <b>WCHAR</b>s that includes the terminating <b>NULL</b>.

### -param pszNetwork [out]

Output buffer for returning the value of the 
      <a href="/previous-versions/windows/desktop/mscs/ip-addresses-network">Network</a> private property.

### -param pcchNetwork [in, out]

On input, specifies the size of the <i>pszNetwork</i> buffer as a count of 
      <b>WCHAR</b>s. On output, specifies the size of the resulting data as a count of 
      <b>WCHAR</b>s that includes the terminating <b>NULL</b>.

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This parameter is named <i>pcch</i> prior to Windows Server 2012.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following are possible error 
       codes.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
<dt>259 (0x103)</dt>
</dl>
</td>
<td width="60%">
No IP Address dependency was found in the specified resource's list of dependencies.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RESOURCE_NOT_PRESENT</b></dt>
<dt>4316 (0x10DC)</dt>
</dl>
</td>
<td width="60%">
No IP Address dependency was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
<dt>234 (0xEA)</dt>
</dl>
</td>
<td width="60%">
The size of one of the buffers was too small to hold the resulting data.

</td>
</tr>
</table>

## -remarks

Do not call 
    <b>ResUtilGetResourceDependentIPAddressProps</b> 
    from any resource DLL entry point function. 
    <b>ResUtilGetResourceDependentIPAddressProps</b> 
    can safely be called from a worker thread. For more information, see 
    <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

The 
    <b>ResUtilGetResourceDependentIPAddressProps</b> 
    function returns only the private properties for the first IPv4 resource that the resource directly depends on. The 
    function does not examine indirect dependencies (such as a resource that depends on a 
    <a href="/previous-versions/windows/desktop/mscs/network-name">network Name</a> resource that in turn depends on an 
    <a href="/previous-versions/windows/desktop/mscs/ip-address">IP Address</a> resource), 
    <a href="/previous-versions/windows/desktop/mscs/ipv6-address">IPv6 Address</a> resources, or 
    <a href="/previous-versions/windows/desktop/mscs/ipv6-tunnel-address">IPv6 Tunnel Address</a> resources.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilfinddependentdiskresourcedriveletter">ResUtilFindDependentDiskResourceDriveLetter</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependency">ResUtilGetResourceDependency</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependencybyclass">ResUtilGetResourceDependencyByClass</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependencybyname">ResUtilGetResourceDependencyByName</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcenamedependency">ResUtilGetResourceNameDependency</a>



<a href="/previous-versions/windows/desktop/mscs/resource-utility-functions">Resource Utility Functions</a>
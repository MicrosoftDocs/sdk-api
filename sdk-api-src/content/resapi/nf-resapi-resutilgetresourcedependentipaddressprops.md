---
UID: NF:resapi.ResUtilGetResourceDependentIPAddressProps
title: ResUtilGetResourceDependentIPAddressProps function (resapi.h)
author: windows-sdk-content
description: Retrieves the private properties of the first IP Address dependency found for a specified resource. The PRESUTIL_GET_RESOURCE_DEPENDENTIP_ADDRESS_PROPS type defines a pointer to this function.
old-location: mscs\resutilgetresourcedependentipaddressprops.htm
tech.root: MsCS
ms.assetid: 283b0086-1dbf-45dc-9651-93af9a9ff6d0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PRESUTIL_GET_RESOURCE_DEPENDENTIP_ADDRESS_PROPS, PRESUTIL_GET_RESOURCE_DEPENDENTIP_ADDRESS_PROPS function [Failover Cluster], ResUtilGetResourceDependentIPAddressProps, ResUtilGetResourceDependentIPAddressProps function [Failover Cluster], _wolf_resutilgetresourcedependentipaddressprops, mscs.resutilgetresourcedependentipaddressprops, resapi/PRESUTIL_GET_RESOURCE_DEPENDENTIP_ADDRESS_PROPS, resapi/ResUtilGetResourceDependentIPAddressProps
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
 - ResUtilGetResourceDependentIPAddressProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilGetResourceDependentIPAddressProps function


## -description


Retrieves the <a href="https://msdn.microsoft.com/a1dee11c-f1fe-4509-a40a-a58c4b8999ef">private properties</a> of the 
    first IP Address <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependency</a> found for a specified 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. The <b>PRESUTIL_GET_RESOURCE_DEPENDENTIP_ADDRESS_PROPS</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the resource to query for dependencies.


### -param pszAddress [out]

Output buffer for returning the value of the 
      <a href="https://msdn.microsoft.com/514eb8f9-55c7-411b-b6ec-8373903f8f17">Address</a> private property.


### -param pcchAddress [in, out]

On input, specifies the size of the <i>pszAddress</i> buffer as a count of 
      <b>WCHAR</b>s. On output, specifies the size of the resulting data as a count of 
      <b>WCHAR</b>s that includes the terminating <b>NULL</b>.


### -param pszSubnetMask [out]

Output buffer for returning the value of the 
      <a href="https://msdn.microsoft.com/413d0d3c-1bb9-4570-ac18-23644f5e7804">SubnetMask</a> private property.


### -param pcchSubnetMask [in, out]

On input, specifies the size of the <i>pszSubnetMask</i> buffer as a count of 
      <b>WCHAR</b>s. On output, specifies the size of the resulting data as a count of 
      <b>WCHAR</b>s that includes the terminating <b>NULL</b>.


### -param pszNetwork [out]

Output buffer for returning the value of the 
      <a href="https://msdn.microsoft.com/61e64153-7d4c-4328-8bb3-8356993d6461">Network</a> private property.


### -param pcchNetwork [in, out]

On input, specifies the size of the <i>pszNetwork</i> buffer as a count of 
      <b>WCHAR</b>s. On output, specifies the size of the resulting data as a count of 
      <b>WCHAR</b>s that includes the terminating <b>NULL</b>.

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This parameter is named <i>pcch</i> prior to Windows Server 2012.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error 
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
    <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.

The 
    <b>ResUtilGetResourceDependentIPAddressProps</b> 
    function returns only the private properties for the first IPv4 resource that the resource directly depends on. The 
    function does not examine indirect dependencies (such as a resource that depends on a 
    <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">network Name</a> resource that in turn depends on an 
    <a href="https://msdn.microsoft.com/3ed966f1-0177-4376-a36d-4a2fda327470">IP Address</a> resource), 
    <a href="https://msdn.microsoft.com/1f91dc67-f3c9-4345-9710-addab2ab1a4d">IPv6 Address</a> resources, or 
    <a href="https://msdn.microsoft.com/e59df4d3-d30b-4d23-853f-d71644c932f7">IPv6 Tunnel Address</a> resources.




## -see-also




<a href="https://msdn.microsoft.com/8f2187e3-6bb7-4756-af2b-a28857581bcb">ResUtilFindDependentDiskResourceDriveLetter</a>



<a href="https://msdn.microsoft.com/eee267b4-4272-4938-b061-02990ec528f2">ResUtilGetResourceDependency</a>



<a href="https://msdn.microsoft.com/7c2bd24a-8034-4a5f-8218-0a23d5e29b07">ResUtilGetResourceDependencyByClass</a>



<a href="https://msdn.microsoft.com/8c978b27-fd1a-47b6-8a30-cfe6e4fbcf57">ResUtilGetResourceDependencyByName</a>



<a href="https://msdn.microsoft.com/071f11bb-fcb3-4c76-ad81-b19ff7bdcb4a">ResUtilGetResourceNameDependency</a>



<a href="https://msdn.microsoft.com/42eb7c1b-6bd6-4997-b33e-ed16470c8475">Resource Utility Functions</a>
 

 


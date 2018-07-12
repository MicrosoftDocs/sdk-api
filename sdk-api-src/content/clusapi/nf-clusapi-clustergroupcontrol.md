---
UID: NF:clusapi.ClusterGroupControl
title: ClusterGroupControl function
author: windows-sdk-content
description: Initiates an operation that affects a group. The operation performed depends on the control code passed to the dwControlCode parameter.
old-location: mscs\clustergroupcontrol.htm
old-project: mscs
ms.assetid: 72896685-a1db-43d7-a5e3-ba380c0624f2
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ClusterGroupControl, ClusterGroupControl function [Failover Cluster], _wolf_clustergroupcontrol, clusapi/ClusterGroupControl, mscs.clustergroupcontrol
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterGroupControl
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterGroupControl function


## -description


Initiates an 
    operation that affects a <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a>. The operation performed depends on 
    the <a href="https://msdn.microsoft.com/47618915-0985-4415-b7d4-5959fb27eb9f">control code</a> passed to the 
    <i>dwControlCode</i> parameter.


## -parameters




### -param hGroup [in]

Handle to the group to be affected.


### -param hHostNode [in, optional]

If non-<b>NULL</b>, handle to the node to perform the operation represented by the control 
       code. If <b>NULL</b>, the <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> that owns the 
       group performs the operation. Specifying <i>hHostNode</i> is optional.


### -param dwControlCode [in]

A <a href="https://msdn.microsoft.com/41f93d49-c021-4fcb-9d38-f801702b9e51">group control code</a> specifying the operation to 
       be performed. For the syntax associated with a control code, refer to  
       <a href="https://msdn.microsoft.com/d107f743-8ce8-4c0c-b7a2-24a70ffbc0f3">Control Code Architecture</a> and the following 
       topics:


<ul>
<li>
<a href="https://msdn.microsoft.com/5d5f2956-8289-48df-903b-47163ae5c1ae">CLUSCTL_GROUP_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/78a77a38-d301-452b-a11a-cf42eaf46532">CLUSCTL_GROUP_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e01103a4-b527-4b8b-9933-7dbe0e6f2ddd">CLUSCTL_GROUP_GET_CHARACTERISTICS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f00cd260-48aa-4e55-a2d6-079f82840da5">CLUSCTL_GROUP_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a95fb950-c2e9-4fd0-8382-f49f802c07d6">CLUSCTL_GROUP_GET_COMMON_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0daffb5e-f63c-48ef-8fe3-f17aa6181386">CLUSCTL_GROUP_GET_FLAGS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f755dc21-2fee-4a48-8f23-02b0a8543c59">CLUSCTL_GROUP_GET_ID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/af2a4c7b-e720-45a8-a12a-827b819fb9cc">CLUSCTL_GROUP_GET_NAME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/aa82f5ca-3f04-47ec-b037-769eddce94d7">CLUSCTL_GROUP_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/39c7ba30-5985-423c-b2a8-081c6693471e">CLUSCTL_GROUP_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2ada0f26-36c3-4b16-a135-0ccd53fd9bdb">CLUSCTL_GROUP_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b01bd00d-f3c4-4087-befc-3c1f1f75a8ab">CLUSCTL_GROUP_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7daddba1-2849-46c1-8ae2-2fd426702afd">CLUSCTL_GROUP_QUERY_DELETE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/854acb91-28df-431d-a6ed-ade4d319d41f">CLUSCTL_GROUP_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a0043a00-5f5a-4088-935f-c4b0cc90ea9d">CLUSCTL_GROUP_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ab34ed81-bd84-4940-8571-91402487b983">CLUSCTL_GROUP_UNKNOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/60fd243c-517c-48f9-9a66-dd4c8bf67703">CLUSCTL_GROUP_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f311df2e-6a43-40e3-98ee-e6a1316734a1">CLUSCTL_GROUP_VALIDATE_PRIVATE_PROPERTIES</a>
</li>
</ul>



### -param lpInBuffer [in, optional]

Pointer to an input buffer containing information needed for the operation, or <b>NULL</b> 
       if no information is needed.


### -param nInBufferSize [in]

The allocated size (in bytes) of the input buffer.


### -param lpOutBuffer [out, optional]

Pointer to an output buffer to receive the data resulting from the operation, or 
       <b>NULL</b> if no data will be returned.


### -param nOutBufferSize [in]

The allocated size (in bytes) of the output buffer.


### -param lpBytesReturned [out, optional]

Returns the actual size (in bytes) of the data resulting from the operation. If this information is not 
       needed, pass <b>NULL</b> for <i>lpBytesReturned</i>.


## -returns



The function returns one of the following values.




## -remarks



If <b>ClusterGroupControl</b> returns 
     <b>ERROR_MORE_DATA</b>, set <i>nOutBufferSize</i> to the number of bytes 
     pointed to by <i>lpBytesReturned</i> and call the function again.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/0fdb2024-9b04-4a38-baf9-3cdabba9bf8c">LPC and RPC Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.

<b>ClusterGroupControl</b> is one of the 
     <a href="https://msdn.microsoft.com/89ae667e-6ad9-453e-b370-b3d6a67172a2">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="https://msdn.microsoft.com/20f87f60-6237-459a-93bc-f599391e65b0">Using Control Codes</a>.


#### Examples

The following code fragment demonstrates a call to 
      <b>ClusterGroupControl</b>.

<pre class="syntax" xml:space="preserve"><code>// Allocate buffer.
lpPropList = LocalAlloc( LPTR, cbAllocated );

// Initial call.
dwResult = ClusterGroupControl( hCluster,
                                NULL,
                                CLUSCTL_GROUP_GET_COMMON_PROPERTIES, 
                                NULL,
                                0,
                                lpPropList,
                                cbAllocated,
                                &amp;cbReturned );

// If the buffer was too small, reallocate it to the necessary size,
// returned in cbReturned.
if ( dwResult == ERROR_MORE_DATA )
{
  LocalFree( lpPropList );
  cbAllocated = cbReturned;
  lpPropList = LocalAlloc( LPTR, cbAllocated );
  if ( lpPropList == NULL )
  {
    // Respond to error.
  }
  dwResult = ClusterGroupControl( hCluster,
                                  NULL,
                                  CLUSCTL_GROUP_GET_COMMON_PROPERTIES,
                                  NULL,
                                  0,
                                  lpPropList,
                                  cbAllocated,
                                  &amp;cbReturned );
}

if ( dwResult != ERROR_SUCCESS )
{
  // Respond to error.
}</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/41f93d49-c021-4fcb-9d38-f801702b9e51">Group Control Codes</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>
 

 


---
UID: NF:clusapi.ClusterGroupControl
title: ClusterGroupControl function
author: windows-sdk-content
description: Initiates an operation that affects a group. The operation performed depends on the control code passed to the dwControlCode parameter.
old-location: mscs\clustergroupcontrol.htm
tech.root: mscs
ms.assetid: 72896685-a1db-43d7-a5e3-ba380c0624f2
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ClusterGroupControl, ClusterGroupControl function [Failover Cluster], _wolf_clustergroupcontrol, clusapi/ClusterGroupControl, mscs.clustergroupcontrol
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# ClusterGroupControl function


## -description


Initiates an 
    operation that affects a <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a>. The operation performed depends on 
    the <a href="https://msdn.microsoft.com/en-us/library/Aa369307(v=VS.85).aspx">control code</a> passed to the 
    <i>dwControlCode</i> parameter.


## -parameters




### -param hGroup [in]

Handle to the group to be affected.


### -param hHostNode [in, optional]

If non-<b>NULL</b>, handle to the node to perform the operation represented by the control 
       code. If <b>NULL</b>, the <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> that owns the 
       group performs the operation. Specifying <i>hHostNode</i> is optional.


### -param dwControlCode [in]

A <a href="https://msdn.microsoft.com/en-us/library/Aa369684(v=VS.85).aspx">group control code</a> specifying the operation to 
       be performed. For the syntax associated with a control code, refer to  
       <a href="https://msdn.microsoft.com/en-us/library/Aa369308(v=VS.85).aspx">Control Code Architecture</a> and the following 
       topics:


<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367236(v=VS.85).aspx">CLUSCTL_GROUP_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367237(v=VS.85).aspx">CLUSCTL_GROUP_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367238(v=VS.85).aspx">CLUSCTL_GROUP_GET_CHARACTERISTICS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367239(v=VS.85).aspx">CLUSCTL_GROUP_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367240(v=VS.85).aspx">CLUSCTL_GROUP_GET_COMMON_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367242(v=VS.85).aspx">CLUSCTL_GROUP_GET_FLAGS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367244(v=VS.85).aspx">CLUSCTL_GROUP_GET_ID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367245(v=VS.85).aspx">CLUSCTL_GROUP_GET_NAME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367246(v=VS.85).aspx">CLUSCTL_GROUP_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367247(v=VS.85).aspx">CLUSCTL_GROUP_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367248(v=VS.85).aspx">CLUSCTL_GROUP_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367249(v=VS.85).aspx">CLUSCTL_GROUP_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367250(v=VS.85).aspx">CLUSCTL_GROUP_QUERY_DELETE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367251(v=VS.85).aspx">CLUSCTL_GROUP_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367252(v=VS.85).aspx">CLUSCTL_GROUP_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367253(v=VS.85).aspx">CLUSCTL_GROUP_UNKNOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367254(v=VS.85).aspx">CLUSCTL_GROUP_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa367255(v=VS.85).aspx">CLUSCTL_GROUP_VALIDATE_PRIVATE_PROPERTIES</a>
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
     <a href="https://msdn.microsoft.com/en-us/library/Aa370974(v=VS.85).aspx">LPC and RPC Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.

<b>ClusterGroupControl</b> is one of the 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369310(v=VS.85).aspx">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa372956(v=VS.85).aspx">Using Control Codes</a>.


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
 

 


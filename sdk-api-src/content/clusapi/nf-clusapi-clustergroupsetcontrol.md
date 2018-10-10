---
UID: NF:clusapi.ClusterGroupSetControl
title: ClusterGroupSetControl function
author: windows-sdk-content
description: Initiates an operation affecting a groupset.
old-location: mscs\clustergroupcollectioncontrol.htm
tech.root: MsCS
ms.assetid: 20f0f70a-b300-41b8-b215-e5a3f24db44b
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ClusterGroupSetControl, ClusterGroupSetControl function [Failover Cluster], PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL, PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL function [Failover Cluster], clusapi/ClusterGroupSetControl, clusapi/PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL, mscs.clustergroupcollectioncontrol
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
api_name:
 - ClusterGroupSetControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterGroupSetControl function


## -description


Initiates an operation affecting a groupset.

The 
    operation performed depends on the <a href="https://msdn.microsoft.com/en-us/library/Aa369307(v=VS.85).aspx">control code</a> passed to the 
    <i>dwControlCode</i> parameter.


## -parameters




### -param hGroupSet [in]

Handle to the groupset to be affected.


### -param hHostNode [in, optional]

If non-<b>NULL</b>, handle to the node to perform the operation represented by the control 
       code. If <b>NULL</b>, the <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> that owns the 
       groupset performs the operation. Specifying <i>hHostNode</i> is optional.


### -param dwControlCode [in]

A <a href="https://msdn.microsoft.com/en-us/library/Mt705457(v=VS.85).aspx">Collection Control Code</a> specifying 
       the operation to be performed. For the syntax associated with a control code, refer to  
       <a href="https://msdn.microsoft.com/en-us/library/Aa369308(v=VS.85).aspx">Control Code Architecture</a> and the following 
       topics.

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Mt705417(v=VS.85).aspx">CLUSCTL_GROUPSET_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Mt705418(v=VS.85).aspx">CLUSCTL_GROUPSET_GET_GROUPS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Mt705420(v=VS.85).aspx">CLUSCTL_GROUPSET_GET_PROVIDER_GROUPS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Mt705419(v=VS.85).aspx">CLUSCTL_GROUPSET_GET_PROVIDER_COLLECTIONS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Mt705421(v=VS.85).aspx">CLUSCTL_GROUPSET_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Mt705422(v=VS.85).aspx">CLUSCTL_GROUPSET_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Mt705424(v=VS.85).aspx">CLUSCTL_GROUP_GET_PROVIDER_GROUPS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Mt705423(v=VS.85).aspx">CLUSCTL_GROUP_GET_PROVIDER_COLLECTIONS</a>
</li>
</ul>

### -param lpInBuffer [in, optional]

Pointer to an input buffer containing information needed for the operation, or <b>NULL</b> 
       if no information is needed.


### -param cbInBufferSize [in]

The allocated size (in bytes) of the input buffer.


### -param lpOutBuffer [out, optional]

Pointer to an output buffer to receive the data resulting from the operation, or 
       <b>NULL</b> if no data will be returned.


### -param cbOutBufferSize [in]

The allocated size (in bytes) of the output buffer.


### -param lpBytesReturned [out, optional]

Returns the actual size (in bytes) of the data resulting from the operation. If this information is not 
       needed, pass <b>NULL</b> for <i>lpBytesReturned</i>.


## -returns



The function returns one of the following values.




---
UID: NC:clusapi.PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL
title: PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL
author: windows-driver-content
description: Initiates an operation affecting a groupset.
old-location: mscs\clustergroupcollectioncontrol.htm
old-project: MsCS
ms.assetid: 20f0f70a-b300-41b8-b215-e5a3f24db44b
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL, PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL callback, PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL callback function [Failover Cluster], clusapi/PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL, mscs.clustergroupcollectioncontrol
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_CLUSTER_GROUP_GROUPSET_CONTROL callback function


## -description


Initiates an operation affecting a groupset.

The 
    operation performed depends on the <a href="https://msdn.microsoft.com/47618915-0985-4415-b7d4-5959fb27eb9f">control code</a> passed to the 
    <i>dwControlCode</i> parameter.


## -parameters




### -param hGroupSet [in]

Handle to the groupset to be affected.


### -param hHostNode [in, optional]

If non-<b>NULL</b>, handle to the node to perform the operation represented by the control 
       code. If <b>NULL</b>, the <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> that owns the 
       groupset performs the operation. Specifying <i>hHostNode</i> is optional.


### -param dwControlCode [in]

A <a href="https://msdn.microsoft.com/85DD2E41-B5DA-41E8-ACD8-2BE283CCF67A">Collection Control Code</a> specifying 
       the operation to be performed. For the syntax associated with a control code, refer to  
       <a href="https://msdn.microsoft.com/d107f743-8ce8-4c0c-b7a2-24a70ffbc0f3">Control Code Architecture</a> and the following 
       topics.

<ul>
<li>
<a href="https://msdn.microsoft.com/CC8D848F-645B-4B26-8E70-DED95F25681B">CLUSCTL_GROUPSET_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/96C75F3B-F9E6-4557-BF41-C8F9D1E1EE3A">CLUSCTL_GROUPSET_GET_GROUPS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8C2AE592-67C9-4E57-B762-A95759F28538">CLUSCTL_GROUPSET_GET_PROVIDER_GROUPS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/76222551-F27D-4354-8B4B-C9FA5EE55C22">CLUSCTL_GROUPSET_GET_PROVIDER_COLLECTIONS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/F3410FAC-2FC0-4C59-BCB1-DED4DD63D5D8">CLUSCTL_GROUPSET_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/B2C0D9C6-C26E-4A56-A15E-243ED6429C8E">CLUSCTL_GROUPSET_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63347D0A-3C5B-4BC6-BE64-79E40D115F7B">CLUSCTL_GROUP_GET_PROVIDER_GROUPS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C51FDDBC-5E32-4950-9A1E-64843F184172">CLUSCTL_GROUP_GET_PROVIDER_COLLECTIONS</a>
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




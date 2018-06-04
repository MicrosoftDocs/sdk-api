---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _QOS_DS_CLASS structure


## -description


The traffic control object 
<b>QOS_DS_CLASS</b> enables application developers to override the default Diffserv code point (DSCP) value for the IP packets associated with a given flow. By default, the DSCP value is derived from the flow's ServiceType.


## -struct-fields




### -field ObjectHdr

The QOS object 
<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>. The object type for this traffic control object should be 
<b>QOS_OBJECT_DS_CLASS</b>.


### -field DSField

User priority value for the flow. The valid range is 0x00 through 0x3F. The following settings are chosen (by default) when the 
<b>QOS_DS_CLASS</b> traffic control object is not used. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
ServiceTypeBestEffort, ServiceTypeQualitative

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x18</dt>
</dl>
</td>
<td width="60%">
ServiceTypeControlledLoad

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x28</dt>
</dl>
</td>
<td width="60%">
ServiceTypeGuaranteed

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x30</dt>
</dl>
</td>
<td width="60%">
ServiceTypeNetworkControl

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Non-conformant traffic

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/3d1035dc-0e46-46f4-abb3-26100356b60d">QOS_DIFFSERV</a>



<a href="https://msdn.microsoft.com/732cfbec-4175-4397-854f-0d2a930e11bc">QOS_DIFFSERV_RULE</a>



<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>



<a href="https://msdn.microsoft.com/60c6492f-ddcf-401c-8121-2349b89eb223">QOS_TRAFFIC_CLASS</a>
 

 


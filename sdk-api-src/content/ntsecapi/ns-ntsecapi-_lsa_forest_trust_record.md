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

# _LSA_FOREST_TRUST_RECORD structure


## -description


The <b>LSA_FOREST_TRUST_RECORD</b> structure represents a <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> forest trust record.


## -struct-fields




### -field Flags

Flags that control the behavior of the operation.


### -field ForestTrustType


<a href="https://msdn.microsoft.com/8a4a7080-fab0-4ab2-a0b4-e929cce21f0c">LSA_FOREST_TRUST_RECORD_TYPE</a> enumeration that indicates the type of the record. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ForestTrustTopLevelName"></a><a id="foresttrusttoplevelname"></a><a id="FORESTTRUSTTOPLEVELNAME"></a><dl>
<dt><b>ForestTrustTopLevelName</b></dt>
</dl>
</td>
<td width="60%">
Record contains an included top-level name.

</td>
</tr>
<tr>
<td width="40%"><a id="ForestTrustTopLevelNameEx"></a><a id="foresttrusttoplevelnameex"></a><a id="FORESTTRUSTTOPLEVELNAMEEX"></a><dl>
<dt><b>ForestTrustTopLevelNameEx</b></dt>
</dl>
</td>
<td width="60%">
Record contains an excluded top-level name.

</td>
</tr>
<tr>
<td width="40%"><a id="ForestTrustDomainInfo"></a><a id="foresttrustdomaininfo"></a><a id="FORESTTRUSTDOMAININFO"></a><dl>
<dt><b>ForestTrustDomainInfo</b></dt>
</dl>
</td>
<td width="60%">
Record contains an <a href="https://msdn.microsoft.com/c0e06735-ca10-4bee-a45b-6db5b6666e31">LSA_FOREST_TRUST_DOMAIN_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ForestTrustRecordTypeLast"></a><a id="foresttrustrecordtypelast"></a><a id="FORESTTRUSTRECORDTYPELAST"></a><dl>
<dt><b>ForestTrustRecordTypeLast</b></dt>
</dl>
</td>
<td width="60%">
Marks the end of an enumeration.

</td>
</tr>
</table>
 


### -field Time

Time stamp of the record.


### -field ForestTrustData.TopLevelName.case

 


### -field ForestTrustData.TopLevelName.case.ForestTrustTopLevelName

 


### -field ForestTrustData.TopLevelName.case.ForestTrustTopLevelNameEx

 


### -field ForestTrustData.DomainInfo.case

 


### -field ForestTrustData.DomainInfo.case.ForestTrustDomainInfo

 


### -field ForestTrustData.Data.default

 


### -field ForestTrustData.switch_type

 


### -field ForestTrustData.switch_type.LSA_FOREST_TRUST_RECORD_TYPE

 


### -field ForestTrustData.switch_is

 


### -field ForestTrustData.switch_is.ForestTrustType

 


### -field ForestTrustData


### -field ForestTrustData.TopLevelName

Top-level name. This member is used only if the <b>ForestTrustType</b> member is <b>ForestTrustTopLevelName</b> or <b>ForestTrustTopLevelNameEx</b>.


### -field ForestTrustData.DomainInfo

Domain information. This member is used only if the <b>ForestTrustType</b> member is <b>ForestTrustDomainInfo</b>.


### -field ForestTrustData.Data

Binary data. This member is used for unrecognized entries after ForestTrustRecordTypeLast.


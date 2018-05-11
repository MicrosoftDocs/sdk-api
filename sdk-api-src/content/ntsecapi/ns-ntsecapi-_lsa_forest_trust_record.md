---
UID: NS:ntsecapi._LSA_FOREST_TRUST_RECORD
title: "_LSA_FOREST_TRUST_RECORD"
author: windows-driver-content
description: Represents a Local Security Authority forest trust record.
old-location: security\lsa_forest_trust_record.htm
old-project: SecAuthN
ms.assetid: 19b4ee56-664f-4f37-bfc9-129032ebeb22
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PLSA_FOREST_TRUST_RECORD, ForestTrustDomainInfo, ForestTrustRecordTypeLast, ForestTrustTopLevelName, ForestTrustTopLevelNameEx, LSA_FOREST_TRUST_RECORD, LSA_FOREST_TRUST_RECORD structure [Security], PLSA_FOREST_TRUST_RECORD, PLSA_FOREST_TRUST_RECORD structure pointer [Security], _LSA_FOREST_TRUST_INFORMATION, _LSA_FOREST_TRUST_RECORD, ntsecapi/LSA_FOREST_TRUST_RECORD, ntsecapi/PLSA_FOREST_TRUST_RECORD, security.lsa_forest_trust_record"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: LSA_FOREST_TRUST_RECORD, *PLSA_FOREST_TRUST_RECORD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	LSA_FOREST_TRUST_RECORD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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


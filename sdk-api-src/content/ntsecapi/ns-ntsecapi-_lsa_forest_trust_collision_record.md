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

# _LSA_FOREST_TRUST_COLLISION_RECORD structure


## -description


The <b>LSA_FOREST_TRUST_COLLISION_RECORD</b> structure contains information about a <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> forest trust collision.


## -struct-fields




### -field Index

Index of this collision record in the array of <b>LSA_FOREST_TRUST_COLLISION_RECORD</b> structures pointed to by the <b>Entries</b> member of the <a href="https://msdn.microsoft.com/a4a3b040-c074-4756-a30f-408d8bca87ba">LSA_FOREST_TRUST_COLLISION_INFORMATION</a> structure.


### -field Type

Type of the collision. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CollisionTdo"></a><a id="collisiontdo"></a><a id="COLLISIONTDO"></a><dl>
<dt><b>CollisionTdo</b></dt>
</dl>
</td>
<td width="60%">
Collision between <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> objects.

</td>
</tr>
<tr>
<td width="40%"><a id="CollisionXref"></a><a id="collisionxref"></a><a id="COLLISIONXREF"></a><dl>
<dt><b>CollisionXref</b></dt>
</dl>
</td>
<td width="60%">
Collision between cross-references.

</td>
</tr>
<tr>
<td width="40%"><a id="CollisionOther"></a><a id="collisionother"></a><a id="COLLISIONOTHER"></a><dl>
<dt><b>CollisionOther</b></dt>
</dl>
</td>
<td width="60%">
Collision that is not a collision between <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> objects or cross-references.

</td>
</tr>
</table>
 


### -field Flags

Flags that provide more information about the collision. The following table lists the possible values for this member when the <b>Type</b> member is CollisionTdo.



#### LSA_TLN_DISABLED_NEW (0x00000001)



#### LSA_TLN_DISABLED_ADMIN (0x00000002)



#### LSA_TLN_DISABLED_CONFLICT (0x00000004)

The following table lists the possible values for this member when the <b>Type</b> member is CollisionXref.



#### LSA_SID_DISABLED_ADMIN (0x00000001)



#### LSA_SID_DISABLED_CONFLICT (0x00000002)



#### LSA_NB_DISABLED_ADMIN (0x00000004)



#### LSA_NB_DISABLED_CONFLICT (0x00000008)


### -field Name


<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that contains the name of the collision record.


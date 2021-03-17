---
UID: NS:ntsecapi._LSA_FOREST_TRUST_COLLISION_RECORD
title: LSA_FOREST_TRUST_COLLISION_RECORD (ntsecapi.h)
description: Contains information about a Local Security Authority forest trust collision.
helpviewer_keywords: ["*PLSA_FOREST_TRUST_COLLISION_RECORD","CollisionOther","CollisionTdo","CollisionXref","LSA_FOREST_TRUST_COLLISION_RECORD","LSA_FOREST_TRUST_COLLISION_RECORD structure [Security]","LSA_NB_DISABLED_ADMIN","LSA_NB_DISABLED_CONFLICT","LSA_SID_DISABLED_ADMIN","LSA_SID_DISABLED_CONFLICT","LSA_TLN_DISABLED_ADMIN","LSA_TLN_DISABLED_CONFLICT","LSA_TLN_DISABLED_NEW","PLSA_FOREST_TRUST_COLLISION_RECORD","PLSA_FOREST_TRUST_COLLISION_RECORD structure pointer [Security]","_LSA_FOREST_TRUST_COLLISION_RECORD","ntsecapi/LSA_FOREST_TRUST_COLLISION_RECORD","ntsecapi/PLSA_FOREST_TRUST_COLLISION_RECORD","security.lsa_forest_trust_collision_record"]
old-location: security\lsa_forest_trust_collision_record.htm
tech.root: security
ms.assetid: 9f9d2f57-0e7f-4222-be35-e3f026b60e93
ms.date: 12/05/2018
ms.keywords: '*PLSA_FOREST_TRUST_COLLISION_RECORD, CollisionOther, CollisionTdo, CollisionXref, LSA_FOREST_TRUST_COLLISION_RECORD, LSA_FOREST_TRUST_COLLISION_RECORD structure [Security], LSA_NB_DISABLED_ADMIN, LSA_NB_DISABLED_CONFLICT, LSA_SID_DISABLED_ADMIN, LSA_SID_DISABLED_CONFLICT, LSA_TLN_DISABLED_ADMIN, LSA_TLN_DISABLED_CONFLICT, LSA_TLN_DISABLED_NEW, PLSA_FOREST_TRUST_COLLISION_RECORD, PLSA_FOREST_TRUST_COLLISION_RECORD structure pointer [Security], _LSA_FOREST_TRUST_COLLISION_RECORD, ntsecapi/LSA_FOREST_TRUST_COLLISION_RECORD, ntsecapi/PLSA_FOREST_TRUST_COLLISION_RECORD, security.lsa_forest_trust_collision_record'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LSA_FOREST_TRUST_COLLISION_RECORD, *PLSA_FOREST_TRUST_COLLISION_RECORD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LSA_FOREST_TRUST_COLLISION_RECORD
 - ntsecapi/_LSA_FOREST_TRUST_COLLISION_RECORD
 - PLSA_FOREST_TRUST_COLLISION_RECORD
 - ntsecapi/PLSA_FOREST_TRUST_COLLISION_RECORD
 - LSA_FOREST_TRUST_COLLISION_RECORD
 - ntsecapi/LSA_FOREST_TRUST_COLLISION_RECORD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - LSA_FOREST_TRUST_COLLISION_RECORD
---

# LSA_FOREST_TRUST_COLLISION_RECORD structure


## -description

The <b>LSA_FOREST_TRUST_COLLISION_RECORD</b> structure contains information about a <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> forest trust collision.

## -struct-fields

### -field Index

Index of this collision record in the array of <b>LSA_FOREST_TRUST_COLLISION_RECORD</b> structures pointed to by the <b>Entries</b> member of the <a href="/windows/win32/api/ntsecapi/ns-ntsecapi-lsa_forest_trust_collision_information">LSA_FOREST_TRUST_COLLISION_INFORMATION</a> structure.

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
Collision between <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> objects.

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
Collision that is not a collision between <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> objects or cross-references.

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

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that contains the name of the collision record.
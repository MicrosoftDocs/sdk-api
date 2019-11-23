---
UID: NS:aclui._EFFPERM_RESULT_LIST
title: EFFPERM_RESULT_LIST (aclui.h)

description: Lists the effective permissions.
old-location: security\effperm_result_list.htm
tech.root: SecAuthZ
ms.assetid: D83C5632-F67A-42BA-A146-989EBB3B2763

ms.date: 12/05/2018
ms.keywords: '*PEFFPERM_RESULT_LIST, EFFPERM_RESULT_LIST, EFFPERM_RESULT_LIST structure [Security], PEFFPERM_RESULT_LIST, PEFFPERM_RESULT_LIST structure pointer [Security], aclui/EFFPERM_RESULT_LIST, aclui/PEFFPERM_RESULT_LIST, security.effperm_result_list'
ms.topic: struct
f1_keywords:
- aclui/EFFPERM_RESULT_LIST
dev_langs:
 - c++
req.header: aclui.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Aclui.h
api_name:
- EFFPERM_RESULT_LIST
targetos: Windows
req.typenames: EFFPERM_RESULT_LIST, *PEFFPERM_RESULT_LIST
req.redist: 
ms.custom: 19H1
---

# EFFPERM_RESULT_LIST structure


## -description


The <b>EFFPERM_RESULT_LIST</b> structure lists the effective permissions.


## -struct-fields




### -field fEvaluated

Indicates if the effective permissions results have been evaluated.


### -field cObjectTypeListLength

The number of elements in both the <b>pObjectTypeList</b> and <b>pGrantedAccessList</b> members.


### -field pObjectTypeList

A pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-object_type_list">OBJECT_TYPE_LIST</a> structures that specifies the properties and property sets for which access was evaluated.


### -field pGrantedAccessList

A pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> values that specifies the access rights granted for each corresponding object type.


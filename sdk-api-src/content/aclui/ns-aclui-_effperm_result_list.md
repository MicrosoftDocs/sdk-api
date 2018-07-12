---
UID: NS:aclui._EFFPERM_RESULT_LIST
title: "_EFFPERM_RESULT_LIST"
author: windows-sdk-content
description: Lists the effective permissions.
old-location: security\effperm_result_list.htm
old-project: secauthz
ms.assetid: D83C5632-F67A-42BA-A146-989EBB3B2763
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: "*PEFFPERM_RESULT_LIST, EFFPERM_RESULT_LIST, EFFPERM_RESULT_LIST structure [Security], PEFFPERM_RESULT_LIST, PEFFPERM_RESULT_LIST structure pointer [Security], _EFFPERM_RESULT_LIST, aclui/EFFPERM_RESULT_LIST, aclui/PEFFPERM_RESULT_LIST, security.effperm_result_list"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: EFFPERM_RESULT_LIST, *PEFFPERM_RESULT_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Aclui.h
api_name:
 - EFFPERM_RESULT_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _EFFPERM_RESULT_LIST structure


## -description


The <b>EFFPERM_RESULT_LIST</b> structure lists the effective permissions.


## -struct-fields




### -field fEvaluated

Indicates if the effective permissions results have been evaluated.


### -field cObjectTypeListLength

The number of elements in both the <b>pObjectTypeList</b> and <b>pGrantedAccessList</b> members.


### -field pObjectTypeList

A pointer to an array of <a href="https://msdn.microsoft.com/c729ff1a-65f3-4f6f-84dd-5700aead75ce">OBJECT_TYPE_LIST</a> structures that specifies the properties and property sets for which access was evaluated.


### -field pGrantedAccessList

A pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a> values that specifies the access rights granted for each corresponding object type.


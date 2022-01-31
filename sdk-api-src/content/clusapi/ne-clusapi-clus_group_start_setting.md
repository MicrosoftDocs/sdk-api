---
UID: NE:clusapi.__unnamed_enum_4
title: CLUS_GROUP_START_SETTING (clusapi.h)
description: Enumerates the start settings for a cluster group.
helpviewer_keywords: ["CLUS_GROUP_DO_NOT_START","CLUS_GROUP_START_ALLOWED","CLUS_GROUP_START_ALWAYS","CLUS_GROUP_START_SETTING","CLUS_GROUP_START_SETTING enumeration [Failover Cluster]","clusapi/CLUS_GROUP_DO_NOT_START","clusapi/CLUS_GROUP_START_ALLOWED","clusapi/CLUS_GROUP_START_ALWAYS","clusapi/CLUS_GROUP_START_SETTING","msclus/CLUS_GROUP_DO_NOT_START","msclus/CLUS_GROUP_START_ALLOWED","msclus/CLUS_GROUP_START_ALWAYS","msclus/CLUS_GROUP_START_SETTING","mscs.clus_group_start_setting"]
old-location: mscs\clus_group_start_setting.htm
tech.root: MsCS
ms.assetid: 9F0A7B9B-278E-4176-BCA7-6CEEF35AFE2E
ms.date: 12/05/2018
ms.keywords: CLUS_GROUP_DO_NOT_START, CLUS_GROUP_START_ALLOWED, CLUS_GROUP_START_ALWAYS, CLUS_GROUP_START_SETTING, CLUS_GROUP_START_SETTING enumeration [Failover Cluster], clusapi/CLUS_GROUP_DO_NOT_START, clusapi/CLUS_GROUP_START_ALLOWED, clusapi/CLUS_GROUP_START_ALWAYS, clusapi/CLUS_GROUP_START_SETTING, msclus/CLUS_GROUP_DO_NOT_START, msclus/CLUS_GROUP_START_ALLOWED, msclus/CLUS_GROUP_START_ALWAYS, msclus/CLUS_GROUP_START_SETTING, mscs.clus_group_start_setting
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: CLUS_GROUP_START_SETTING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_GROUP_START_SETTING
 - clusapi/CLUS_GROUP_START_SETTING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUS_GROUP_START_SETTING
---

# CLUS_GROUP_START_SETTING enumeration


## -description

Enumerates the start settings for a cluster group.

## -enum-fields

### -field CLUS_GROUP_START_ALWAYS:0

Always start the cluster.

### -field CLUS_GROUP_DO_NOT_START:1

Do not start the cluster.

### -field CLUS_GROUP_START_ALLOWED:2

The cluster can be started.


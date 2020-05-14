---
UID: NS:projectedfslib.PRJ_VIRTUALIZATION_INSTANCE_INFO
title: PRJ_VIRTUALIZATION_INSTANCE_INFO (projectedfslib.h)
description: Information about a virtualization instance.helpviewer_keywords: ["PRJ_VIRTUALIZATION_INSTANCE_INFO","PRJ_VIRTUALIZATION_INSTANCE_INFO structure","ProjFS.prj_virtualization_instance_info","projectedfslib/PRJ_VIRTUALIZATION_INSTANCE_INFO"]
old-location: projfs\prj_virtualization_instance_info.htm
tech.root: ProjFS
ms.assetid: B6532FDF-F190-4C10-BF5C-96BDF477BB4A
ms.date: 12/05/2018
ms.keywords: PRJ_VIRTUALIZATION_INSTANCE_INFO, PRJ_VIRTUALIZATION_INSTANCE_INFO structure, ProjFS.prj_virtualization_instance_info, projectedfslib/PRJ_VIRTUALIZATION_INSTANCE_INFO
f1_keywords:
- projectedfslib/PRJ_VIRTUALIZATION_INSTANCE_INFO
dev_langs:
- c++
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
- projectedfslib.h
api_name:
- PRJ_VIRTUALIZATION_INSTANCE_INFO
targetos: Windows
req.typenames: PRJ_VIRTUALIZATION_INSTANCE_INFO
req.redist: 
ms.custom: RS5, 19H1
---

# PRJ_VIRTUALIZATION_INSTANCE_INFO structure


## -description


Information about a virtualization instance.


## -struct-fields




### -field InstanceID

An ID corresponding to a specific virtualization instance.


### -field WriteAlignment

The value used for the byteOffset and length parameters of <a href="https://docs.microsoft.com/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwritefiledata">PrjWriteFileData</a>.


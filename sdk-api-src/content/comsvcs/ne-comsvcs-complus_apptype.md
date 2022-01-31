---
UID: NE:comsvcs.tagCOMPLUS_APPTYPE
title: COMPLUS_APPTYPE (comsvcs.h)
description: Represents types of applications tracked by the tracker server.
helpviewer_keywords: ["APPTYPE_LIBRARY","APPTYPE_SERVER","APPTYPE_SWC","APPTYPE_UNKNOWN","COMPLUS_APPTYPE","COMPLUS_APPTYPE enumeration [COM+]","comsvcs/APPTYPE_LIBRARY","comsvcs/APPTYPE_SERVER","comsvcs/APPTYPE_SWC","comsvcs/APPTYPE_UNKNOWN","comsvcs/COMPLUS_APPTYPE","cos.complus_apptype"]
old-location: cos\complus_apptype.htm
tech.root: cos
ms.assetid: 121d287f-067b-4640-ac81-43904463ded4
ms.date: 12/05/2018
ms.keywords: APPTYPE_LIBRARY, APPTYPE_SERVER, APPTYPE_SWC, APPTYPE_UNKNOWN, COMPLUS_APPTYPE, COMPLUS_APPTYPE enumeration [COM+], comsvcs/APPTYPE_LIBRARY, comsvcs/APPTYPE_SERVER, comsvcs/APPTYPE_SWC, comsvcs/APPTYPE_UNKNOWN, comsvcs/COMPLUS_APPTYPE, cos.complus_apptype
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: COMPLUS_APPTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCOMPLUS_APPTYPE
 - comsvcs/tagCOMPLUS_APPTYPE
 - COMPLUS_APPTYPE
 - comsvcs/COMPLUS_APPTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - COMPLUS_APPTYPE
---

# COMPLUS_APPTYPE enumeration


## -description

Represents types of applications tracked by the tracker server.

## -enum-fields

### -field APPTYPE_UNKNOWN:0xffffffff

This value is not used.

### -field APPTYPE_SERVER:1

COM+ server application.

### -field APPTYPE_LIBRARY:0

COM+ library application.

### -field APPTYPE_SWC:2

COM+ services without components.

## -see-also

<a href="/windows/desktop/api/comsvcs/ns-comsvcs-applicationprocesssummary">ApplicationProcessSummary</a>



<a href="/windows/desktop/api/comsvcs/ns-comsvcs-applicationsummary">ApplicationSummary</a>

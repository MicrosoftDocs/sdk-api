---
UID: NE:ndattrib.tagREPAIR_SCOPE
title: tagREPAIR_SCOPE
author: windows-sdk-content
description: The REPAIR_SCOPE enumeration describes the scope of modification for a given repair.
old-location: ndf\repair_scope.htm
tech.root: NDF
ms.assetid: f9be87ae-82a1-4613-abeb-15ccba1bf360
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PREPAIR_SCOPE, REPAIR_SCOPE, REPAIR_SCOPE enumeration [NDF], RS_APPLICATION, RS_PROCESS, RS_SYSTEM, RS_USER, ndattrib/REPAIR_SCOPE, ndattrib/RS_APPLICATION, ndattrib/RS_PROCESS, ndattrib/RS_SYSTEM, ndattrib/RS_USER, ndf.repair_scope, tagREPAIR_SCOPE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ndattrib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Ndattrib.h
api_name:
 - REPAIR_SCOPE
product: Windows
targetos: Windows
req.typenames: REPAIR_SCOPE, *PREPAIR_SCOPE
req.redist: 
---

# tagREPAIR_SCOPE enumeration


## -description


The <b>REPAIR_SCOPE</b> enumeration describes the scope of modification for a given repair.


## -enum-fields




### -field RS_SYSTEM

The repair effect is system-wide.


### -field RS_USER

The repair effect is user-specific.


### -field RS_APPLICATION

The repair effect is application-specific.


### -field RS_PROCESS

The repair effect is process-specific.


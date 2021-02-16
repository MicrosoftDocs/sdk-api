---
UID: NS:setupapi._INFCONTEXT
title: INFCONTEXT (setupapi.h)
description: The INFCONTEXT structure stores context information that functions such as SetupGetLineText use to navigate INF files.
helpviewer_keywords: ["*PINFCONTEXT","INFCONTEXT","INFCONTEXT structure [Setup API]","PINFCONTEXT","PINFCONTEXT structure pointer [Setup API]","_setupapi_infcontext_str","setup.infcontext_str","setupapi/INFCONTEXT","setupapi/PINFCONTEXT"]
old-location: setup\infcontext_str.htm
tech.root: setup
ms.assetid: 5b3d32a8-e651-4017-aaa7-b532ec47da53
ms.date: 12/05/2018
ms.keywords: '*PINFCONTEXT, INFCONTEXT, INFCONTEXT structure [Setup API], PINFCONTEXT, PINFCONTEXT structure pointer [Setup API], _setupapi_infcontext_str, setup.infcontext_str, setupapi/INFCONTEXT, setupapi/PINFCONTEXT'
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: INFCONTEXT, *PINFCONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INFCONTEXT
 - setupapi/_INFCONTEXT
 - PINFCONTEXT
 - setupapi/PINFCONTEXT
 - INFCONTEXT
 - setupapi/INFCONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Setupapi.h
api_name:
 - INFCONTEXT
---

# INFCONTEXT structure


## -description

The 
<b>INFCONTEXT</b> structure stores context information that functions such as 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetlinetexta">SetupGetLineText</a> use to navigate INF files.

## -struct-fields

### -field Inf

Handle to the INF file returned by 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopeninffilea">SetupOpenInfFile</a>.

### -field CurrentInf

Pointer to the current INF file. The <b>Inf</b> member may point to multiple files if they were appended to the open INF file using 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupopenappendinffilea">SetupOpenAppendInfFile</a>.

### -field Section

Section in the current INF file.

### -field Line

Line of the current section in the INF file. 




<div class="alert"><b>Note</b>    The setup functions use this structure internally and it must not be accessed or modified by applications. It is included here for informational purposes only.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupfindfirstlinea">SetupFindFirstLine</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupfindnextline">SetupFindNextLine</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupfindnextmatchlinea">SetupFindNextMatchLine</a>



<a href="/windows/desktop/SetupApi/structures--setup-api-">Structures</a>
---
UID: NS:lpmapi.GuarRspec
title: GuarRspec (lpmapi.h)
description: The GuarRspec structure contains guaranteed Rspec information.
helpviewer_keywords: ["GuarRspec","GuarRspec structure [QOS]","lpmapi/GuarRspec","qos.guarrspec"]
old-location: qos\guarrspec.htm
tech.root: QOS
ms.assetid: b5a2daa1-9783-44c2-baa6-5164dedf498f
ms.date: 12/05/2018
ms.keywords: GuarRspec, GuarRspec structure [QOS], lpmapi/GuarRspec, qos.guarrspec
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: GuarRspec
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GuarRspec
 - lpmapi/GuarRspec
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - GuarRspec
---

# GuarRspec structure


## -description

The 
<b>GuarRspec</b> structure contains guaranteed Rspec information.

## -struct-fields

### -field Guar_R

Guaranteed rate, in bytes per second.

### -field Guar_S

Slack term, in  seconds.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-guarflowspec">GuarFlowSpec</a>


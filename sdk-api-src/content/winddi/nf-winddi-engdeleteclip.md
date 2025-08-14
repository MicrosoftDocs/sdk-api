---
UID: NF:winddi.EngDeleteClip
title: EngDeleteClip function (winddi.h)
description: The EngDeleteClip function deletes a CLIPOBJ structure allocated by EngCreateClip.
helpviewer_keywords: ["EngDeleteClip","EngDeleteClip function [Display Devices]","display.engdeleteclip","gdifncs_0ca10e14-e720-49f3-8c56-9c9dd646f04f.xml","winddi/EngDeleteClip"]
old-location: display\engdeleteclip.htm
tech.root: display
ms.assetid: 7af85df1-1e37-4a69-82a0-1c1eec32dd48
ms.date: 12/05/2018
ms.keywords: EngDeleteClip, EngDeleteClip function [Display Devices], display.engdeleteclip, gdifncs_0ca10e14-e720-49f3-8c56-9c9dd646f04f.xml, winddi/EngDeleteClip
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngDeleteClip
 - winddi/EngDeleteClip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngDeleteClip
---

# EngDeleteClip function


## -description

The <b>EngDeleteClip</b> function deletes a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure allocated by <a href="/windows/desktop/api/winddi/nf-winddi-engcreateclip">EngCreateClip</a>.

## -parameters

### -param pco

Pointer to the CLIPOBJ structure to delete.

## -returns

None
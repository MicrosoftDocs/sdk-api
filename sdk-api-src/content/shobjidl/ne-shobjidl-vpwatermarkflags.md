---
UID: NE:shobjidl.VPWATERMARKFLAGS
title: VPWATERMARKFLAGS (shobjidl.h)
description: Specifies watermark flags. Used by IVisualProperties::SetWatermark.
helpviewer_keywords: ["VPWATERMARKFLAGS","VPWATERMARKFLAGS enumeration [Windows Shell]","VPWF_ALPHABLEND","VPWF_DEFAULT","_shell_VPWATERMARKFLAGS","shell.VPWATERMARKFLAGS","shobjidl/VPWATERMARKFLAGS","shobjidl/VPWF_ALPHABLEND","shobjidl/VPWF_DEFAULT"]
old-location: shell\VPWATERMARKFLAGS.htm
tech.root: shell
ms.assetid: e54db88e-c334-442b-8ab5-6004176aab41
ms.date: 12/05/2018
ms.keywords: VPWATERMARKFLAGS, VPWATERMARKFLAGS enumeration [Windows Shell], VPWF_ALPHABLEND, VPWF_DEFAULT, _shell_VPWATERMARKFLAGS, shell.VPWATERMARKFLAGS, shobjidl/VPWATERMARKFLAGS, shobjidl/VPWF_ALPHABLEND, shobjidl/VPWF_DEFAULT
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VPWATERMARKFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VPWATERMARKFLAGS
 - shobjidl/VPWATERMARKFLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl.h
api_name:
 - VPWATERMARKFLAGS
---

# VPWATERMARKFLAGS enumeration


## -description

Specifies watermark flags. Used by <a href="/windows/desktop/api/shobjidl/nf-shobjidl-ivisualproperties-setwatermark">IVisualProperties::SetWatermark</a>.

## -enum-fields

### -field VPWF_DEFAULT:0

Default Windows XP behavior.

### -field VPWF_ALPHABLEND:0x1

Alpha blend the respective bitmap; assumed 24-bit color + 8-bit alpha.

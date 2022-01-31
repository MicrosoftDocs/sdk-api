---
UID: NE:wmcontainer.MFASF_SPLITTERFLAGS
title: MFASF_SPLITTERFLAGS (wmcontainer.h)
description: Defines the ASF splitter options.
helpviewer_keywords: ["8eaad139-b487-4348-ae19-4251a2aeed14","MFASF_SPLITTERFLAGS","MFASF_SPLITTERFLAGS enumeration [Media Foundation]","MFASF_SPLITTER_REVERSE","MFASF_SPLITTER_WMDRM","enumeration [Media Foundation]","mf.mfasf_splitterflags","wmcontainer/MFASF_SPLITTERFLAGS","wmcontainer/MFASF_SPLITTER_REVERSE","wmcontainer/MFASF_SPLITTER_WMDRM"]
old-location: mf\mfasf_splitterflags.htm
tech.root: mf
ms.assetid: 8eaad139-b487-4348-ae19-4251a2aeed14
ms.date: 12/05/2018
ms.keywords: 8eaad139-b487-4348-ae19-4251a2aeed14, MFASF_SPLITTERFLAGS, MFASF_SPLITTERFLAGS enumeration [Media Foundation], MFASF_SPLITTER_REVERSE, MFASF_SPLITTER_WMDRM, enumeration [Media Foundation], mf.mfasf_splitterflags, wmcontainer/MFASF_SPLITTERFLAGS, wmcontainer/MFASF_SPLITTER_REVERSE, wmcontainer/MFASF_SPLITTER_WMDRM
req.header: wmcontainer.h
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
targetos: Windows
req.typenames: MFASF_SPLITTERFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFASF_SPLITTERFLAGS
 - wmcontainer/MFASF_SPLITTERFLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmcontainer.h
api_name:
 - MFASF_SPLITTERFLAGS
---

# MFASF_SPLITTERFLAGS enumeration


## -description

Defines the ASF splitter options.

## -enum-fields

### -field MFASF_SPLITTER_REVERSE:0x1

The splitter delivers samples for the ASF content in reverse order to accommodate reverse playback.

### -field MFASF_SPLITTER_WMDRM:0x2

The splitter delivers samples for streams that are protected with Windows Media Digital Rights Management.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>

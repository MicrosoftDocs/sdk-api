---
UID: NE:wmcontainer.ASF_STATUSFLAGS
title: ASF_STATUSFLAGS (wmcontainer.h)
description: Defines status conditions for the IMFASFSplitter::GetNextSample method.
helpviewer_keywords: ["ASF_STATUSFLAGS","ASF_STATUSFLAGS enumeration [Media Foundation]","ASF_STATUSFLAGS_INCOMPLETE","ASF_STATUSFLAGS_NONFATAL_ERROR","c8f1944a-2b61-4c6e-8c87-37c2985fbdca","mf.asf_statusflags","wmcontainer/ASF_STATUSFLAGS","wmcontainer/ASF_STATUSFLAGS_INCOMPLETE","wmcontainer/ASF_STATUSFLAGS_NONFATAL_ERROR"]
old-location: mf\asf_statusflags.htm
tech.root: mf
ms.assetid: c8f1944a-2b61-4c6e-8c87-37c2985fbdca
ms.date: 12/05/2018
ms.keywords: ASF_STATUSFLAGS, ASF_STATUSFLAGS enumeration [Media Foundation], ASF_STATUSFLAGS_INCOMPLETE, ASF_STATUSFLAGS_NONFATAL_ERROR, c8f1944a-2b61-4c6e-8c87-37c2985fbdca, mf.asf_statusflags, wmcontainer/ASF_STATUSFLAGS, wmcontainer/ASF_STATUSFLAGS_INCOMPLETE, wmcontainer/ASF_STATUSFLAGS_NONFATAL_ERROR
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
req.typenames: ASF_STATUSFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ASF_STATUSFLAGS
 - wmcontainer/ASF_STATUSFLAGS
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
 - ASF_STATUSFLAGS
---

# ASF_STATUSFLAGS enumeration


## -description

Defines status conditions for the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample">IMFASFSplitter::GetNextSample</a> method.

## -enum-fields

### -field ASF_STATUSFLAGS_INCOMPLETE:0x1

The operation is incomplete.

### -field ASF_STATUSFLAGS_NONFATAL_ERROR:0x2

 One or more non-critical errors
        occurred while parsing the ASF data.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>

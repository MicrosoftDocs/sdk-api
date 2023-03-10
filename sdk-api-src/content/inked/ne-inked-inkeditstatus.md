---
UID: NE:inked.InkEditStatus
title: InkEditStatus (inked.h)
description: Specifies whether the InkEdit control is idle, collecting ink, or recognizing ink.
helpviewer_keywords: ["94c3a863-4c8a-4471-be1b-b4d5f8ded374","IES_Collecting","IES_Idle","IES_Recognizing","InkEditStatus","InkEditStatus enumeration [Tablet PC]","inked/IES_Collecting","inked/IES_Idle","inked/IES_Recognizing","inked/InkEditStatus","tablet.inkeditstatus"]
old-location: tablet\inkeditstatus.htm
tech.root: tablet
ms.assetid: 94c3a863-4c8a-4471-be1b-b4d5f8ded374
ms.date: 12/05/2018
ms.keywords: 94c3a863-4c8a-4471-be1b-b4d5f8ded374, IES_Collecting, IES_Idle, IES_Recognizing, InkEditStatus, InkEditStatus enumeration [Tablet PC], inked/IES_Collecting, inked/IES_Idle, inked/IES_Recognizing, inked/InkEditStatus, tablet.inkeditstatus
req.header: inked.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: InkEditStatus
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkEditStatus
 - inked/InkEditStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - inked.h
api_name:
 - InkEditStatus
---

# InkEditStatus enumeration


## -description

Specifies whether the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control is idle, collecting ink, or recognizing ink.

## -enum-fields

### -field IES_Idle:0

The <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control is neither collecting nor recognizing ink.

### -field IES_Collecting:1

The <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control is collecting ink.

### -field IES_Recognizing:2

The <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control is recognizing ink.

## -see-also

<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit Control Reference</a>



<a href="/windows/desktop/tablet/inkedit-messages--win32-only-">InkEdit Messages</a>



<a href="/windows/desktop/api/inked/nf-inked-iinkedit-get_status">Status Property</a>

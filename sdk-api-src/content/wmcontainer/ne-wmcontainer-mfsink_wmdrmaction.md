---
UID: NE:wmcontainer._MFSINK_WMDRMACTION
title: MFSINK_WMDRMACTION (wmcontainer.h)
description: Specifies how the ASF file sink should apply Windows Media DRM.
helpviewer_keywords: ["MFSINK_WMDRMACTION","MFSINK_WMDRMACTION enumeration [Media Foundation]","MFSINK_WMDRMACTION_ENCODE","MFSINK_WMDRMACTION_LAST","MFSINK_WMDRMACTION_TRANSCODE","MFSINK_WMDRMACTION_TRANSCRYPT","MFSINK_WMDRMACTION_UNDEFINED","d7c0e63f-236c-4d3c-b5fd-51befa2b54e7","mf.mfsink_wmdrmaction","wmcontainer/MFSINK_WMDRMACTION","wmcontainer/MFSINK_WMDRMACTION_ENCODE","wmcontainer/MFSINK_WMDRMACTION_LAST","wmcontainer/MFSINK_WMDRMACTION_TRANSCODE","wmcontainer/MFSINK_WMDRMACTION_TRANSCRYPT","wmcontainer/MFSINK_WMDRMACTION_UNDEFINED"]
old-location: mf\mfsink_wmdrmaction.htm
tech.root: mf
ms.assetid: d7c0e63f-236c-4d3c-b5fd-51befa2b54e7
ms.date: 12/05/2018
ms.keywords: MFSINK_WMDRMACTION, MFSINK_WMDRMACTION enumeration [Media Foundation], MFSINK_WMDRMACTION_ENCODE, MFSINK_WMDRMACTION_LAST, MFSINK_WMDRMACTION_TRANSCODE, MFSINK_WMDRMACTION_TRANSCRYPT, MFSINK_WMDRMACTION_UNDEFINED, d7c0e63f-236c-4d3c-b5fd-51befa2b54e7, mf.mfsink_wmdrmaction, wmcontainer/MFSINK_WMDRMACTION, wmcontainer/MFSINK_WMDRMACTION_ENCODE, wmcontainer/MFSINK_WMDRMACTION_LAST, wmcontainer/MFSINK_WMDRMACTION_TRANSCODE, wmcontainer/MFSINK_WMDRMACTION_TRANSCRYPT, wmcontainer/MFSINK_WMDRMACTION_UNDEFINED
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
req.typenames: MFSINK_WMDRMACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFSINK_WMDRMACTION
 - wmcontainer/_MFSINK_WMDRMACTION
 - MFSINK_WMDRMACTION
 - wmcontainer/MFSINK_WMDRMACTION
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
 - MFSINK_WMDRMACTION
---

# MFSINK_WMDRMACTION enumeration


## -description

Specifies how the ASF file sink should apply Windows Media DRM.

## -enum-fields

### -field MFSINK_WMDRMACTION_UNDEFINED:0

Undefined action.

### -field MFSINK_WMDRMACTION_ENCODE:1

Encode the content using Windows Media DRM. Use this flag if the source content does not have DRM protection.

### -field MFSINK_WMDRMACTION_TRANSCODE:2

Transcode the content using Windows Media DRM. Use this flag if the source content has Windows Media DRM protection and you want to change the encoding parameters but not the DRM protection.

### -field MFSINK_WMDRMACTION_TRANSCRYPT:3

Transcrypt the content. Use this flag if the source content has DRM protection and you want to change the DRM protection; for example, if you want to convert from Windows Media DRM version 1 to Windows Media DRM version 7 or later.

### -field MFSINK_WMDRMACTION_LAST:3

Reserved. Do not use.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>

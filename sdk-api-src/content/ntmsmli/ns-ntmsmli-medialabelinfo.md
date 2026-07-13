---
UID: NS:ntmsmli.MediaLabelInfo
title: MediaLabelInfo (ntmsmli.h)
description: The MediaLabelInfo structure conveys information to the RSM database about a tape OMID. The media label library fills in this structure for all media labels the library recognizes.
helpviewer_keywords: ["*pMediaLabelInfo","MediaLabelInfo","MediaLabelInfo structure [Files]","_zaw_medialabelinfo","base.medialabelinfo","fs.medialabelinfo","ntmsmli/MediaLabelInfo"]
old-location: fs\medialabelinfo.htm
tech.root: fs
ms.assetid: 8641e9e6-e251-4bf9-935a-f8888705f9a1
ms.date: 12/05/2018
ms.keywords: '*pMediaLabelInfo, MediaLabelInfo, MediaLabelInfo structure [Files], _zaw_medialabelinfo, base.medialabelinfo, fs.medialabelinfo, ntmsmli/MediaLabelInfo'
req.header: ntmsmli.h
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
req.typenames: MediaLabelInfo, *pMediaLabelInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - pMediaLabelInfo
 - ntmsmli/pMediaLabelInfo
 - MediaLabelInfo
 - ntmsmli/MediaLabelInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NtmsMli.h
api_name:
 - MediaLabelInfo
---

# MediaLabelInfo structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>MediaLabelInfo</b> structure conveys information to the RSM database about a tape OMID. The media label library fills in this structure for all media labels the library recognizes.

## -struct-fields

### -field LabelType

Unicode string that identifies the source of the media label. Often this is the name of the backup application or Windows command that wrote the label,
for example, "Microsoft Windows Wbadmin".

### -field LabelIDSize

Number of bytes that are used in the <b>LabelID</b> member.

### -field LabelID

Unique identifier for the media label.

### -field LabelAppDescr

Unicode string that describes the media. For example, the description for a backup media label would be similar to "Tape created on 04/14/97".

## -see-also

<a href="/windows/desktop/api/ntmsmli/nc-ntmsmli-claimmedialabel">ClaimMediaLabel</a>


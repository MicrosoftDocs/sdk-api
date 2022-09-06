---
UID: NE:segment.DVDSPExt
title: DVDSPExt (segment.h)
description: The DVDSPExt enumeration type holds a value indicating the default DVD subpicture language extension.
helpviewer_keywords: ["DVDSPExt","DVDSPExt enumeration [Microsoft TV Technologies]","dvdSPExt_CC_Big","dvdSPExt_CC_Children","dvdSPExt_CC_Normal","dvdSPExt_Caption_Big","dvdSPExt_Caption_Children","dvdSPExt_Caption_Normal","dvdSPExt_DirectorComments_Big","dvdSPExt_DirectorComments_Children","dvdSPExt_DirectorComments_Normal","dvdSPExt_Forced","dvdSPExt_NotSpecified","enumeration [Microsoft TV Technologies]","mstv.dvdspext","segment/DVDSPExt","segment/dvdSPExt_CC_Big","segment/dvdSPExt_CC_Children","segment/dvdSPExt_CC_Normal","segment/dvdSPExt_Caption_Big","segment/dvdSPExt_Caption_Children","segment/dvdSPExt_Caption_Normal","segment/dvdSPExt_DirectorComments_Big","segment/dvdSPExt_DirectorComments_Children","segment/dvdSPExt_DirectorComments_Normal","segment/dvdSPExt_Forced","segment/dvdSPExt_NotSpecified"]
old-location: mstv\dvdspext.htm
tech.root: mstv
ms.assetid: cc33083a-1281-4863-937c-bd4688989a6c
ms.date: 12/05/2018
ms.keywords: DVDSPExt, DVDSPExt enumeration [Microsoft TV Technologies], dvdSPExt_CC_Big, dvdSPExt_CC_Children, dvdSPExt_CC_Normal, dvdSPExt_Caption_Big, dvdSPExt_Caption_Children, dvdSPExt_Caption_Normal, dvdSPExt_DirectorComments_Big, dvdSPExt_DirectorComments_Children, dvdSPExt_DirectorComments_Normal, dvdSPExt_Forced, dvdSPExt_NotSpecified, enumeration [Microsoft TV Technologies], mstv.dvdspext, segment/DVDSPExt, segment/dvdSPExt_CC_Big, segment/dvdSPExt_CC_Children, segment/dvdSPExt_CC_Normal, segment/dvdSPExt_Caption_Big, segment/dvdSPExt_Caption_Children, segment/dvdSPExt_Caption_Normal, segment/dvdSPExt_DirectorComments_Big, segment/dvdSPExt_DirectorComments_Children, segment/dvdSPExt_DirectorComments_Normal, segment/dvdSPExt_Forced, segment/dvdSPExt_NotSpecified
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DVDSPExt
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DVDSPExt
 - segment/DVDSPExt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - segment.h
api_name:
 - DVDSPExt
---

# DVDSPExt enumeration


## -description

The <b>DVDSPExt</b> enumeration type holds a value indicating the default DVD subpicture language extension.

## -enum-fields

### -field dvdSPExt_NotSpecified:0

Extension not specified.

### -field dvdSPExt_Caption_Normal:1

Normal caption size.

### -field dvdSPExt_Caption_Big:2

Big captions.

### -field dvdSPExt_Caption_Children:3

Children's captions.

### -field dvdSPExt_CC_Normal:5

Normal-sized closed captions.

### -field dvdSPExt_CC_Big:6

Big closed captions.

### -field dvdSPExt_CC_Children:7

Children's closed captions.

### -field dvdSPExt_Forced:9

Forced.

### -field dvdSPExt_DirectorComments_Normal:13

Normal-sized director's comments.

### -field dvdSPExt_DirectorComments_Big:14

Big director's comments.

### -field dvdSPExt_DirectorComments_Children:15

Director's comments for children.

## -see-also

<a href="/previous-versions/dd695197(v=vs.85)">DefaultSubpictureLanguageExt</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectdefaultsubpicturelanguage">SelectDefaultSubpictureLanguage</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-enumerations">Video Control Enumerations</a>

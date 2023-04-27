---
UID: NE:strmif.tagDVD_SUBPICTURE_LANG_EXT
title: DVD_SUBPICTURE_LANG_EXT (strmif.h)
description: Defines the possible language extensions in a specified subpicture stream.
helpviewer_keywords: ["DVD_SP_EXT_CC_Big","DVD_SP_EXT_CC_Children","DVD_SP_EXT_CC_Normal","DVD_SP_EXT_Caption_Big","DVD_SP_EXT_Caption_Children","DVD_SP_EXT_Caption_Normal","DVD_SP_EXT_DirectorComments_Big","DVD_SP_EXT_DirectorComments_Children","DVD_SP_EXT_DirectorComments_Normal","DVD_SP_EXT_Forced","DVD_SP_EXT_NotSpecified","DVD_SUBPICTURE_LANG_EXT","DVD_SUBPICTURE_LANG_EXT","DVD_SUBPICTURE_LANG_EXT enumeration [DirectShow]","DVD_SUBPICTURE_LANG_EXTEnumeration","dshow.dvd_subpicture_lang_ext","strmif/DVD_SP_EXT_CC_Big","strmif/DVD_SP_EXT_CC_Children","strmif/DVD_SP_EXT_CC_Normal","strmif/DVD_SP_EXT_Caption_Big","strmif/DVD_SP_EXT_Caption_Children","strmif/DVD_SP_EXT_Caption_Normal","strmif/DVD_SP_EXT_DirectorComments_Big","strmif/DVD_SP_EXT_DirectorComments_Children","strmif/DVD_SP_EXT_DirectorComments_Normal","strmif/DVD_SP_EXT_Forced","strmif/DVD_SP_EXT_NotSpecified","strmif/DVD_SUBPICTURE_LANG_EXT"]
old-location: dshow\dvd_subpicture_lang_ext.htm
tech.root: dshow
ms.assetid: 314c6187-a475-44c9-b22a-b168211fceb3
ms.date: 12/05/2018
ms.keywords: DVD_SP_EXT_CC_Big, DVD_SP_EXT_CC_Children, DVD_SP_EXT_CC_Normal, DVD_SP_EXT_Caption_Big, DVD_SP_EXT_Caption_Children, DVD_SP_EXT_Caption_Normal, DVD_SP_EXT_DirectorComments_Big, DVD_SP_EXT_DirectorComments_Children, DVD_SP_EXT_DirectorComments_Normal, DVD_SP_EXT_Forced, DVD_SP_EXT_NotSpecified, DVD_SUBPICTURE_LANG_EXT, DVD_SUBPICTURE_LANG_EXT , DVD_SUBPICTURE_LANG_EXT enumeration [DirectShow], DVD_SUBPICTURE_LANG_EXTEnumeration, dshow.dvd_subpicture_lang_ext, strmif/DVD_SP_EXT_CC_Big, strmif/DVD_SP_EXT_CC_Children, strmif/DVD_SP_EXT_CC_Normal, strmif/DVD_SP_EXT_Caption_Big, strmif/DVD_SP_EXT_Caption_Children, strmif/DVD_SP_EXT_Caption_Normal, strmif/DVD_SP_EXT_DirectorComments_Big, strmif/DVD_SP_EXT_DirectorComments_Children, strmif/DVD_SP_EXT_DirectorComments_Normal, strmif/DVD_SP_EXT_Forced, strmif/DVD_SP_EXT_NotSpecified, strmif/DVD_SUBPICTURE_LANG_EXT
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DVD_SUBPICTURE_LANG_EXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_SUBPICTURE_LANG_EXT
 - strmif/tagDVD_SUBPICTURE_LANG_EXT
 - DVD_SUBPICTURE_LANG_EXT
 - strmif/DVD_SUBPICTURE_LANG_EXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_SUBPICTURE_LANG_EXT
---

# DVD_SUBPICTURE_LANG_EXT enumeration


## -description

Defines the possible language extensions in a specified subpicture stream.

## -enum-fields

### -field DVD_SP_EXT_NotSpecified:0

Indicates that no language extensions are present.

### -field DVD_SP_EXT_Caption_Normal:1

Indicates that the specified stream contains normal captions.

### -field DVD_SP_EXT_Caption_Big:2

Indicates that the specified stream contains big captions.

### -field DVD_SP_EXT_Caption_Children:3

Indicates that the specified stream contains captions for children.

### -field DVD_SP_EXT_CC_Normal:5

Indicates that the specified stream contains normal closed captions.

### -field DVD_SP_EXT_CC_Big:6

Indicates that the specified stream contains big closed captions.

### -field DVD_SP_EXT_CC_Children:7

Indicates that the specified stream contains closed captions for children.

### -field DVD_SP_EXT_Forced:9

Indicates that the subpicture stream is forcedly activated, meaning that the application will not be able to turn it off.

### -field DVD_SP_EXT_DirectorComments_Normal:13

Indicates that the specified stream contains normal-sized director's comments.

### -field DVD_SP_EXT_DirectorComments_Big:14

Indicates that the specified stream contains large-sized director's comments.

### -field DVD_SP_EXT_DirectorComments_Children:15

Indicates that the specified stream contains director's comments for children.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectdefaultsubpicturelanguage">IDvdControl2::SelectDefaultSubpictureLanguage</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdefaultsubpicturelanguage">IDvdInfo2::GetDefaultSubpictureLanguage</a>

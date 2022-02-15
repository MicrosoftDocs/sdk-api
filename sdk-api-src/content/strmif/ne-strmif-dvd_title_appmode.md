---
UID: NE:strmif.tagDVD_TITLE_APPMODE
title: DVD_TITLE_APPMODE (strmif.h)
description: Indicates whether a DVD title is a karaoke title. This enumeration is a member of the DVD_TitleAttributes structure, which is filled when an application calls the IDvdInfo2::GetTitleAttributes method.
helpviewer_keywords: ["DVD_AppMode_Karaoke","DVD_AppMode_Not_Specified","DVD_AppMode_Other","DVD_TITLE_APPMODE","DVD_TITLE_APPMODE","DVD_TITLE_APPMODE enumeration [DirectShow]","DVD_TITLE_APPMODEEnumeration","dshow.dvd_title_appmode","strmif/DVD_AppMode_Karaoke","strmif/DVD_AppMode_Not_Specified","strmif/DVD_AppMode_Other","strmif/DVD_TITLE_APPMODE"]
old-location: dshow\dvd_title_appmode.htm
tech.root: dshow
ms.assetid: f0a12b00-89a5-4b70-9a78-519ae36d1bac
ms.date: 12/05/2018
ms.keywords: DVD_AppMode_Karaoke, DVD_AppMode_Not_Specified, DVD_AppMode_Other, DVD_TITLE_APPMODE, DVD_TITLE_APPMODE , DVD_TITLE_APPMODE enumeration [DirectShow], DVD_TITLE_APPMODEEnumeration, dshow.dvd_title_appmode, strmif/DVD_AppMode_Karaoke, strmif/DVD_AppMode_Not_Specified, strmif/DVD_AppMode_Other, strmif/DVD_TITLE_APPMODE
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
req.typenames: DVD_TITLE_APPMODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_TITLE_APPMODE
 - strmif/tagDVD_TITLE_APPMODE
 - DVD_TITLE_APPMODE
 - strmif/DVD_TITLE_APPMODE
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
 - DVD_TITLE_APPMODE
---

# DVD_TITLE_APPMODE enumeration


## -description

Indicates whether a DVD title is a karaoke title. This enumeration is a member of the [DVD_TitleAttributes](/windows/desktop/api/strmif/ns-strmif-dvd_titleattributes) structure, which is filled when an application calls the <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-gettitleattributes">IDvdInfo2::GetTitleAttributes</a> method.

## -enum-fields

### -field DVD_AppMode_Not_Specified:0

The disc does not provide any application mode information about this title.

### -field DVD_AppMode_Karaoke:1

Title contains karaoke content.

### -field DVD_AppMode_Other:3

Title contains a type of content that the <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator Filter</a> does not recognize, so the application should treat the title as a regular DVD-Video title.

## -remarks

When the DVD Navigator encounters a karaoke title on a disc, it goes into "karaoke mode" and informs the audio decoder. The decoder must respond by initially muting the three auxiliary channels. Applications can then selectively control the volume and mixing configuration of these channels using the karaoke-related methods in the <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> interface For more information, see <a href="/windows/desktop/DirectShow/playing-karaoke-audio-streams">Playing Karaoke Audio Streams</a>.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>

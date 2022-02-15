---
UID: NE:strmif.tagDVD_DOMAIN
title: DVD_DOMAIN (strmif.h)
description: Defines the DVD domains.
helpviewer_keywords: ["DVD_DOMAIN","DVD_DOMAIN","DVD_DOMAIN enumeration [DirectShow]","DVD_DOMAINEnumeration","DVD_DOMAIN_FirstPlay","DVD_DOMAIN_Stop","DVD_DOMAIN_Title","DVD_DOMAIN_VideoManagerMenu","DVD_DOMAIN_VideoTitleSetMenu","dshow.dvd_domain","strmif/DVD_DOMAIN","strmif/DVD_DOMAIN_FirstPlay","strmif/DVD_DOMAIN_Stop","strmif/DVD_DOMAIN_Title","strmif/DVD_DOMAIN_VideoManagerMenu","strmif/DVD_DOMAIN_VideoTitleSetMenu"]
old-location: dshow\dvd_domain.htm
tech.root: dshow
ms.assetid: 2763a159-d4de-44c2-905b-5828f328cbd2
ms.date: 12/05/2018
ms.keywords: DVD_DOMAIN, DVD_DOMAIN , DVD_DOMAIN enumeration [DirectShow], DVD_DOMAINEnumeration, DVD_DOMAIN_FirstPlay, DVD_DOMAIN_Stop, DVD_DOMAIN_Title, DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, dshow.dvd_domain, strmif/DVD_DOMAIN, strmif/DVD_DOMAIN_FirstPlay, strmif/DVD_DOMAIN_Stop, strmif/DVD_DOMAIN_Title, strmif/DVD_DOMAIN_VideoManagerMenu, strmif/DVD_DOMAIN_VideoTitleSetMenu
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
req.typenames: DVD_DOMAIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_DOMAIN
 - strmif/tagDVD_DOMAIN
 - DVD_DOMAIN
 - strmif/DVD_DOMAIN
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
 - DVD_DOMAIN
---

# DVD_DOMAIN enumeration


## -description

Defines the DVD domains.

## -enum-fields

### -field DVD_DOMAIN_FirstPlay:1

Performing default initialization of a DVD disc.

### -field DVD_DOMAIN_VideoManagerMenu

Displaying menus for whole disc.

### -field DVD_DOMAIN_VideoTitleSetMenu

Displaying menus for current title set.

### -field DVD_DOMAIN_Title

Displaying the current title.

### -field DVD_DOMAIN_Stop

The DVD Navigator is in the DVD Stop domain.

## -remarks

This enumeration is used in the <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getcurrentdomain">IDvdInfo2::GetCurrentDomain</a> method.

A domain is a logical space on a DVD disc. When the DVD Navigator is displaying the disc's main menu, it is said to be in the Video Manager domain. When it is displaying a menu specific to a title, it is in the Video Title Set domain. When it is playing video, it is the Title domain. When the user issues a Stop command, the Navigator goes into the Stop domain.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getcurrentdomain">IDvdInfo2::GetCurrentDomain</a>

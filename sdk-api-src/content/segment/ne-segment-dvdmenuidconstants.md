---
UID: NE:segment.DVDMenuIDConstants
title: DVDMenuIDConstants (segment.h)
description: The DVDMenuID constants define menu type ID numbers used to display specific menus.
helpviewer_keywords: ["DVDMenuID Constants","DVDMenuIDConstants","DVDMenuIDConstants enumeration [Microsoft TV Technologies]","DVDMenuIDConstantsEnumeration","dvdMenu_Angle","dvdMenu_Audio","dvdMenu_Chapter","dvdMenu_Root","dvdMenu_Subpicture","dvdMenu_Title","enumeration [Microsoft TV Technologies]","mstv.dvdmenuid_constants","segment/","segment/dvdMenu_Angle","segment/dvdMenu_Audio","segment/dvdMenu_Chapter","segment/dvdMenu_Root","segment/dvdMenu_Subpicture","segment/dvdMenu_Title"]
old-location: mstv\dvdmenuid_constants.htm
tech.root: mstv
ms.assetid: f58ce7b6-6fc4-4766-bf8a-180a5568d27c
ms.date: 12/05/2018
ms.keywords: DVDMenuID Constants, DVDMenuIDConstants, DVDMenuIDConstants enumeration [Microsoft TV Technologies], DVDMenuIDConstantsEnumeration, dvdMenu_Angle, dvdMenu_Audio, dvdMenu_Chapter, dvdMenu_Root, dvdMenu_Subpicture, dvdMenu_Title, enumeration [Microsoft TV Technologies], mstv.dvdmenuid_constants, segment/, segment/dvdMenu_Angle, segment/dvdMenu_Audio, segment/dvdMenu_Chapter, segment/dvdMenu_Root, segment/dvdMenu_Subpicture, segment/dvdMenu_Title
req.header: segment.h
req.include-header: Msvidctl.h
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
req.typenames: DVDMenuIDConstants
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DVDMenuIDConstants
 - segment/DVDMenuIDConstants
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Segment.h
api_name:
 - DVDMenuIDConstants
---

# DVDMenuIDConstants enumeration


## -description

The <b>DVDMenuID</b> constants define menu type ID numbers used to display specific menus.

## -enum-fields

### -field dvdMenu_Title:2

Title menu, also called the Video Manager Menu.

### -field dvdMenu_Root

Root menu, the menu for one video title set, which can contain one title or a group of titles.

### -field dvdMenu_Subpicture

Subpicture menu.

### -field dvdMenu_Audio

Audio menu.

### -field dvdMenu_Angle

Angle menu.

### -field dvdMenu_Chapter

Chapter menu.

## -remarks

All the titles in a title set share the same Subpicture, Audio, Angle, and Chapter menus.

## -see-also

<a href="/previous-versions/dd695183(v=vs.85)">MSVidWebDVD Constants</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-showmenu">ShowMenu</a>

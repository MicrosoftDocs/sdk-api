---
UID: NS:shobjidl_core.tagBANDSITEINFO
title: BANDSITEINFO (shobjidl_core.h)
description: Contains information about a band site. This structure is used with the IBandSite::GetBandSiteInfo and IBandSite::SetBandSiteInfo methods.
helpviewer_keywords: ["BANDSITEINFO","BANDSITEINFO structure [Windows Shell]","BSIM_STATE","BSIM_STYLE","BSIS_ALWAYSGRIPPER","BSIS_AUTOGRIPPER","BSIS_FIXEDORDER","BSIS_LEFTALIGN","BSIS_LOCKED","BSIS_NOCAPTION","BSIS_NOCONTEXTMENU","BSIS_NODROPTARGET","BSIS_NOGRIPPER","BSIS_PREFERNOLINEBREAK","BSIS_PRESERVEORDERDURINGLAYOUT","BSIS_SINGLECLICK","BSSF_NOTITLE","BSSF_UNDELETEABLE","BSSF_VISIBLE","_win32_BANDSITEINFO","shell.BANDSITEINFO","shobjidl_core/BANDSITEINFO","tagBANDSITEINFO"]
old-location: shell\BANDSITEINFO.htm
tech.root: shell
ms.assetid: 86e4afce-594a-441e-b6d9-ce05c8234150
ms.date: 12/05/2018
ms.keywords: BANDSITEINFO, BANDSITEINFO structure [Windows Shell], BSIM_STATE, BSIM_STYLE, BSIS_ALWAYSGRIPPER, BSIS_AUTOGRIPPER, BSIS_FIXEDORDER, BSIS_LEFTALIGN, BSIS_LOCKED, BSIS_NOCAPTION, BSIS_NOCONTEXTMENU, BSIS_NODROPTARGET, BSIS_NOGRIPPER, BSIS_PREFERNOLINEBREAK, BSIS_PRESERVEORDERDURINGLAYOUT, BSIS_SINGLECLICK, BSSF_NOTITLE, BSSF_UNDELETEABLE, BSSF_VISIBLE, _win32_BANDSITEINFO, shell.BANDSITEINFO, shobjidl_core/BANDSITEINFO, tagBANDSITEINFO
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BANDSITEINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagBANDSITEINFO
 - shobjidl_core/tagBANDSITEINFO
 - BANDSITEINFO
 - shobjidl_core/BANDSITEINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - BANDSITEINFO
---

# BANDSITEINFO structure


## -description

Contains information about a band site. This structure is used with the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-getbandsiteinfo">IBandSite::GetBandSiteInfo</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-setbandsiteinfo">IBandSite::SetBandSiteInfo</a> methods.

## -struct-fields

### -field dwMask

Type: <b>DWORD</b>

The mask values that determine the other fields in this structure that are being requested or set.



#### BSIM_STATE

The <b>dwState</b> value is being requested or set.



#### BSIM_STYLE

The <b>dwStyle</b> value is being requested or set.

### -field dwState

Type: <b>DWORD</b>

Bits that specify the state of the band.



#### BSSF_VISIBLE

The band is visible.



#### BSSF_NOTITLE

The band's title is not shown.



#### BSSF_UNDELETEABLE

The band cannot be deleted.

### -field dwStyle

Type: <b>DWORD</b>

Bit flags that specify the style of the band.



#### BSIS_AUTOGRIPPER

Show the gripper if the band is neither fixed in size nor floating.



#### BSIS_NOGRIPPER

Equivalent to RBBS_NOGRIPPER.



#### BSIS_ALWAYSGRIPPER

Equivalent to RBBS_GRIPPERALWAYS.



#### BSIS_LEFTALIGN

Equivalent to RBBS_VERTICALGRIPPER.



#### BSIS_SINGLECLICK

Opposite to RBBS_DBLCLKTOGGLE.



#### BSIS_NOCONTEXTMENU

Disables the band-specific context menu (typically "Close Toolbar").



#### BSIS_NODROPTARGET

Prevents wrapping of the <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> interface provided by the band.



#### BSIS_NOCAPTION

Hides the band caption text.



#### BSIS_PREFERNOLINEBREAK

Sets the fAutoBreak member of NMREBARAUTOBREAK to specify the preference of no line break.



#### BSIS_LOCKED

Removes the "Close Toolbar" and "Show Title" choices from the menu.



#### BSIS_PRESERVEORDERDURINGLAYOUT (0x00000200)

<b>Internet Explorer 7 and later</b>. Preserves the order of items during layout.



#### BSIS_FIXEDORDER (0x00000400)

<b>Internet Explorer 7 and later</b>. Prevents items from being reordered.
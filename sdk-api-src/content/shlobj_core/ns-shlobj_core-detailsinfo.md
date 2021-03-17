---
UID: NS:shlobj_core._DETAILSINFO
title: DETAILSINFO (shlobj_core.h)
description: Contains detail information for a Shell folder item. Used with the SFVM_GETDETAILSOF notification.
helpviewer_keywords: ["*PDETAILSINFO","DETAILSINFO","DETAILSINFO structure [Windows Shell]","LVCFMT_CENTER","LVCFMT_COL_HAS_IMAGES","LVCFMT_LEFT","LVCFMT_RIGHT","_DETAILSINFO","_win32_DETAILSINFO","shell.DETAILSINFO","shlobj_core/DETAILSINFO"]
old-location: shell\DETAILSINFO.htm
tech.root: shell
ms.assetid: 255de86e-c3d4-4b1d-9b61-7ee679a4973e
ms.date: 12/05/2018
ms.keywords: '*PDETAILSINFO, DETAILSINFO, DETAILSINFO structure [Windows Shell], LVCFMT_CENTER, LVCFMT_COL_HAS_IMAGES, LVCFMT_LEFT, LVCFMT_RIGHT, _DETAILSINFO, _win32_DETAILSINFO, shell.DETAILSINFO, shlobj_core/DETAILSINFO'
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DETAILSINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DETAILSINFO
 - shlobj_core/_DETAILSINFO
 - DETAILSINFO
 - shlobj_core/DETAILSINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - DETAILSINFO
---

# DETAILSINFO structure


## -description

Contains detail information for a Shell folder item. Used with the <a href="/windows/desktop/shell/sfvm-getdetailsof">SFVM_GETDETAILSOF</a> notification.

## -struct-fields

### -field pidl

Type: <b>PCUITEMID_CHILD</b>

PIDL of the item whose details are being retrieved.

### -field fmt

Type: <b>int</b>

The alignment of the column heading and the subitem text in the column. This member can be one of the following values. Note that the alignment of the leftmost column is always left-justified and cannot be changed.



#### LVCFMT_CENTER

Text is centered.



#### LVCFMT_COL_HAS_IMAGES

Header item contains an image in the image list.



#### LVCFMT_LEFT

Text is left-aligned.



#### LVCFMT_RIGHT

Text is right-aligned.

### -field cxChar

Type: <b>int</b>

The number of average-sized characters in the heading.

### -field str

Type: <b><a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a></b>

An <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure that includes a string containing the requested detail. To convert this structure to a string, use <a href="/windows/desktop/api/shlwapi/nf-shlwapi-strrettobufa">StrRetToBuf</a> or <a href="/windows/desktop/api/shlwapi/nf-shlwapi-strrettostra">StrRetToStr</a>.

### -field iImage

Type: <b>int</b>

The index of an icon in the Shell image list that is displayed in the view.
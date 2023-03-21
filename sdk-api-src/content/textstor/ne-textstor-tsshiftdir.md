---
UID: NE:textstor.__MIDL_IAnchor_0002
title: TsShiftDir (textstor.h)
description: Elements of the TsShiftDir enumeration specify which direction an anchor is moved.
helpviewer_keywords: ["TS_SD_BACKWARD","TS_SD_FORWARD","TsShiftDir","TsShiftDir enumeration [Text Services Framework]","_tsf_tsshiftdir_ref","textstor/TS_SD_BACKWARD","textstor/TS_SD_FORWARD","textstor/TsShiftDir","tsf.tsshiftdir"]
old-location: tsf\tsshiftdir.htm
tech.root: TSF
ms.assetid: e247b79d-354c-4211-9160-e705436d669c
ms.date: 12/05/2018
ms.keywords: TS_SD_BACKWARD, TS_SD_FORWARD, TsShiftDir, TsShiftDir enumeration [Text Services Framework], _tsf_tsshiftdir_ref, textstor/TS_SD_BACKWARD, textstor/TS_SD_FORWARD, textstor/TsShiftDir, tsf.tsshiftdir
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TsShiftDir
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - __MIDL_IAnchor_0002
 - textstor/__MIDL_IAnchor_0002
 - TsShiftDir
 - textstor/TsShiftDir
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Textstor.h
api_name:
 - TsShiftDir
---

# TsShiftDir enumeration


## -description

Elements of the <b>TsShiftDir</b> enumeration specify which direction an anchor is moved.

## -enum-fields

### -field TS_SD_BACKWARD:0

Specifies that the anchor will be moved to the region immediately preceding a range of text.

### -field TS_SD_FORWARD:1

Specifies that the anchor will be moved to the region immediately following a range of text.

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-ianchor-shiftregion">IAnchor::ShiftRegion
      </a>

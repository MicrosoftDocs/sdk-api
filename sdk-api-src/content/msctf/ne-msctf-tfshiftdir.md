---
UID: NE:msctf.__MIDL_ITfRange_0002
title: TfShiftDir (msctf.h)
description: Elements of the TfShiftDir enumeration specify which direction a range anchor is moved.
helpviewer_keywords: ["TF_SD_BACKWARD","TF_SD_FORWARD","TfShiftDir","TfShiftDir enumeration [Text Services Framework]","_tsf_tfshiftdir_ref","msctf/TF_SD_BACKWARD","msctf/TF_SD_FORWARD","msctf/TfShiftDir","tsf.tfshiftdir"]
old-location: tsf\tfshiftdir.htm
tech.root: TSF
ms.assetid: f6a9f9a2-9691-49c7-a481-47ad2cd67a4d
ms.date: 12/05/2018
ms.keywords: TF_SD_BACKWARD, TF_SD_FORWARD, TfShiftDir, TfShiftDir enumeration [Text Services Framework], _tsf_tfshiftdir_ref, msctf/TF_SD_BACKWARD, msctf/TF_SD_FORWARD, msctf/TfShiftDir, tsf.tfshiftdir
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TfShiftDir
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - __MIDL_ITfRange_0002
 - msctf/__MIDL_ITfRange_0002
 - TfShiftDir
 - msctf/TfShiftDir
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msctf.h
api_name:
 - TfShiftDir
---

# TfShiftDir enumeration


## -description

Elements of the <b>TfShiftDir</b> enumeration specify which direction a range anchor is moved.

## -enum-fields

### -field TF_SD_BACKWARD:0

Specifies that the anchor will be moved to the region immediately preceding the range.

### -field TF_SD_FORWARD:1

Specifies that the anchor will be moved to the region immediately following the range.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftendregion">ITfRange::ShiftEndRegion
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftstartregion">ITfRange::ShiftStartRegion
      </a>

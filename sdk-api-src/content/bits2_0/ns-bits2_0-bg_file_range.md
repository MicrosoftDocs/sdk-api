---
UID: NS:bits2_0._BG_FILE_RANGE
title: BG_FILE_RANGE (bits2_0.h)
description: Identifies a range of bytes to download from a file.
helpviewer_keywords: ["BG_FILE_RANGE","BG_FILE_RANGE structure [BITS]","bits.bg_file_range","bits2_0/BG_FILE_RANGE"]
old-location: bits\bg_file_range.htm
tech.root: Bits
ms.assetid: 4ed20321-fb89-410b-906e-9f2c4366645a
ms.date: 12/05/2018
ms.keywords: BG_FILE_RANGE, BG_FILE_RANGE structure [BITS], bits.bg_file_range, bits2_0/BG_FILE_RANGE
req.header: bits2_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2,KB842773 on   Windows Server 2003 and  Windows XP
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits2_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BG_FILE_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BG_FILE_RANGE
 - bits2_0/_BG_FILE_RANGE
 - BG_FILE_RANGE
 - bits2_0/BG_FILE_RANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits2_0.h
api_name:
 - BG_FILE_RANGE
---

# BG_FILE_RANGE structure


## -description

Identifies a range of bytes to download from a file.

## -struct-fields

### -field InitialOffset

Zero-based offset to the beginning of the range of bytes to download from a file.

### -field Length

The length of the range, in bytes. Do not specify a zero byte length. To indicate that the range extends to the end of the file, specify <b>BG_LENGTH_TO_EOF</b>.

## -remarks

The range must exist in the file or BITS generates an <b>BG_E_INVALID_RANGE</b> error.

## -see-also

<a href="/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyfile2-getfileranges">IBackgroundCopyFile2::GetFileRanges</a>



<a href="/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyjob3-addfilewithranges">IBackgroundCopyJob3::AddFileWithRanges</a>
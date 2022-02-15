---
UID: NF:msctf.ITfReverseConversionList.GetLength
title: ITfReverseConversionList::GetLength (msctf.h)
description: Retrieves the number of keystroke sequences in the list.
helpviewer_keywords: ["GetLength","GetLength method [Text Services Framework]","GetLength method [Text Services Framework]","ITfReverseConversionList interface","ITfReverseConversionList interface [Text Services Framework]","GetLength method","ITfReverseConversionList.GetLength","ITfReverseConversionList::GetLength","msctf/ITfReverseConversionList::GetLength","tsf.itfreverseconversionlist_getlength"]
old-location: tsf\itfreverseconversionlist_getlength.htm
tech.root: TSF
ms.assetid: 0cf59b02-486b-412b-a8c2-b8a6e8e50248
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Text Services Framework], GetLength method [Text Services Framework],ITfReverseConversionList interface, ITfReverseConversionList interface [Text Services Framework],GetLength method, ITfReverseConversionList.GetLength, ITfReverseConversionList::GetLength, msctf/ITfReverseConversionList::GetLength, tsf.itfreverseconversionlist_getlength
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 with SP1 [desktop apps only]
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfReverseConversionList::GetLength
 - msctf/ITfReverseConversionList::GetLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfReverseConversionList.GetLength
---

# ITfReverseConversionList::GetLength


## -description

<p class="CCE_Message">[<b>GetLength</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For internal use only.]

Retrieves the number of keystroke sequences in the list.

## -parameters

### -param puIndex [out]

The number of keystroke sequences  in the list.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfreverseconversionlist">ITfReverseConversionList</a>
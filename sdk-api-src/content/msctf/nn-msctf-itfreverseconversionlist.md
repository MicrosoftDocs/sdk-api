---
UID: NN:msctf.ITfReverseConversionList
title: ITfReverseConversionList (msctf.h)
description: Represents a list of the keystroke sequences required to create a specified string.
helpviewer_keywords: ["ITfReverseConversionList","ITfReverseConversionList interface [Text Services Framework]","ITfReverseConversionList interface [Text Services Framework]","described","msctf/ITfReverseConversionList","tsf.itfreverseconversionlist"]
old-location: tsf\itfreverseconversionlist.htm
tech.root: TSF
ms.assetid: 2659bade-af85-42c5-bdb3-32eab16753a8
ms.date: 12/05/2018
ms.keywords: ITfReverseConversionList, ITfReverseConversionList interface [Text Services Framework], ITfReverseConversionList interface [Text Services Framework],described, msctf/ITfReverseConversionList, tsf.itfreverseconversionlist
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
 - ITfReverseConversionList
 - msctf/ITfReverseConversionList
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
 - ITfReverseConversionList
---

# ITfReverseConversionList interface


## -description

<p class="CCE_Message">[<b>ITfReverseConversionList</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For internal use only.]

Represents a list of the keystroke sequences required to create a specified string.

## -inheritance

The <b>ITfReverseConversionList</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfReverseConversionList</b> also has these types of members:

## -remarks

This interface is used to store the results of the <a href="/windows/desktop/api/msctf/nf-msctf-itfreverseconversion-doreverseconversion">ITfReverseConversionList::DoReverseConversion</a> method.

---
UID: NN:imapi2.IBlockRange
title: IBlockRange (imapi2.h)
description: Use this interface to retrieve information about a single continuous range of sectors on the media. This interface is typically used together with the IBlockRangeList interface to describe a collection of sector ranges.
helpviewer_keywords: ["IBlockRange","IBlockRange interface [IMAPI]","IBlockRange interface [IMAPI]","described","imapi.iblockrange","imapi2/IBlockRange"]
old-location: imapi\iblockrange.htm
tech.root: imapi
ms.assetid: abebc651-0575-4b76-9fe8-2cea3d617582
ms.date: 12/05/2018
ms.keywords: IBlockRange, IBlockRange interface [IMAPI], IBlockRange interface [IMAPI],described, imapi.iblockrange, imapi2/IBlockRange
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBlockRange
 - imapi2/IBlockRange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IBlockRange
---

# IBlockRange interface


## -description

Use this interface to retrieve information about a single continuous range of sectors on the media. This interface is typically used together with the <a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist">IBlockRangeList</a> interface to describe a collection of sector ranges.

## -inheritance

The <b>IBlockRange</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IBlockRange</b> also has these types of members:

## -remarks

The values returned by the <a href="/windows/desktop/api/imapi2/nf-imapi2-iblockrange-get_startlba">IBlockRange::get_StartLba</a> and <a href="/windows/desktop/api/imapi2/nf-imapi2-iblockrange-get_endlba">IBlockRange::get_EndLba</a> methods define an inclusive range, i.e. both the start and end sectors belong to the range.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist">IBlockRangeList</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>

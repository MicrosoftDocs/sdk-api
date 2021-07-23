---
UID: NN:imapi2.IBlockRangeList
title: IBlockRangeList (imapi2.h)
description: Use this interface to retrieve a list of continuous sector ranges on the media. This interface is used to describe the sectors that need to be updated on a rewritable disc when a new logical session is recorded.
helpviewer_keywords: ["IBlockRangeList","IBlockRangeList interface [IMAPI]","IBlockRangeList interface [IMAPI]","described","imapi.iblockrangelist","imapi2/IBlockRangeList"]
old-location: imapi\iblockrangelist.htm
tech.root: imapi
ms.assetid: f2a3bd54-4f40-4bf0-9cbf-b507819d669f
ms.date: 12/05/2018
ms.keywords: IBlockRangeList, IBlockRangeList interface [IMAPI], IBlockRangeList interface [IMAPI],described, imapi.iblockrangelist, imapi2/IBlockRangeList
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
 - IBlockRangeList
 - imapi2/IBlockRangeList
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
 - IBlockRangeList
 - IBlockRangeList.get_BlockRanges
---

# IBlockRangeList interface


## -description

Use this interface to retrieve a list of continuous sector ranges on the media. This interface is used to describe the sectors that need to be updated on a rewritable disc when a new logical session is recorded.

## -inheritance

The <b>IBlockRangeList</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IBlockRangeList</b> also has these types of members:

## -remarks

<b>IBlockRangeList</b> is returned by the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimageresult2-get_modifiedblocks">IFileSystemImageResult2::ModifiedBlocks</a> method. Alternatively, IUnknown::QueryInterface can be called on the object returned by <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimageresult-get_imagestream">IFileSystemImageResult::get_ImageStream</a> to get the list of modified sectors in the result image represented by that object.

The order of sector ranges in <b>IBlockRangeList</b> is taken into account during burning. The sector ranges having lower indexes in the safe array returned by <a href="/windows/desktop/api/imapi2/nf-imapi2-iblockrangelist-get_blockranges">IBlockRangeList::get_BlockRanges</a> are written before those with higher indexes.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange">IBlockRange</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>

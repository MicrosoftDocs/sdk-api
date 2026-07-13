---
UID: NN:imapi2fs.IEnumFsiItems
title: IEnumFsiItems (imapi2fs.h)
description: Use this interface to enumerate the child directory and file items for a FsiDirectoryItem object.
helpviewer_keywords: ["IEnumFsiItems","IEnumFsiItems interface [IMAPI]","IEnumFsiItems interface [IMAPI]","described","imapi.ienumfsiitems","imapi2fs/IEnumFsiItems"]
old-location: imapi\ienumfsiitems.htm
tech.root: imapi
ms.assetid: f3186af1-4056-4cb5-aac4-5253ee6dbc01
ms.date: 12/05/2018
ms.keywords: IEnumFsiItems, IEnumFsiItems interface [IMAPI], IEnumFsiItems interface [IMAPI],described, imapi.ienumfsiitems, imapi2fs/IEnumFsiItems
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - IEnumFsiItems
 - imapi2fs/IEnumFsiItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IEnumFsiItems
---

# IEnumFsiItems interface


## -description

Use this interface to enumerate the child directory and file items for a FsiDirectoryItem object.

To get this interface, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-get_enumfsiitems">IFsiDirectoryItem::get_EnumFsiItems</a> method.

## -inheritance

The <b>IEnumFsiItems</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumFsiItems</b> also has these types of members:

## -remarks

This is a <b>EnumFsiItems</b> object in script.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a>

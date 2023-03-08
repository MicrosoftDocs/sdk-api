---
UID: NN:imapi2fs.IProgressItem
title: IProgressItem (imapi2fs.h)
description: Use this interface to retrieve block information for one segment of the result file image.
helpviewer_keywords: ["IProgressItem","IProgressItem interface [IMAPI]","IProgressItem interface [IMAPI]","described","imapi.iprogressitem","imapi2fs/IProgressItem"]
old-location: imapi\iprogressitem.htm
tech.root: imapi
ms.assetid: b6ba9226-655e-4eac-ad43-2b5a8e90039f
ms.date: 12/05/2018
ms.keywords: IProgressItem, IProgressItem interface [IMAPI], IProgressItem interface [IMAPI],described, imapi.iprogressitem, imapi2fs/IProgressItem
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
 - IProgressItem
 - imapi2fs/IProgressItem
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
 - IProgressItem
---

# IProgressItem interface


## -description

Use this interface to retrieve block information for one segment of the result file image. This can be used to determine the LBA ranges of files in the resulting image. This information can then be used to display to the user which file is currently being written to the media or used for other advanced burning functionality.

To get this interface, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-next">IEnumProgressItems::Next</a> or <a href="/windows/desktop/imapi/ienumprogressitems-remotenext">IEnumProgressItems::RemoteNext</a> method.

## -inheritance

The <b>IProgressItem</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IProgressItem</b> also has these types of members:

## -remarks

This is a <b>ProgressItem</b> object in script.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems">IEnumProgressItems</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult">IFileSystemImageResult</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems">IProgressItems</a>

---
UID: NN:imapi2fs.IProgressItems
title: IProgressItems (imapi2fs.h)
description: Use this interface to enumerate the progress items in a result image.
helpviewer_keywords: ["IProgressItems","IProgressItems interface [IMAPI]","IProgressItems interface [IMAPI]","described","imapi.iprogressitems","imapi2fs/IProgressItems"]
old-location: imapi\iprogressitems.htm
tech.root: imapi
ms.assetid: 40c28e67-8ff3-4330-90a1-7ebccb0023ad
ms.date: 12/05/2018
ms.keywords: IProgressItems, IProgressItems interface [IMAPI], IProgressItems interface [IMAPI],described, imapi.iprogressitems, imapi2fs/IProgressItems
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
 - IProgressItems
 - imapi2fs/IProgressItems
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
 - IProgressItems
---

# IProgressItems interface


## -description

Use this interface to enumerate the progress items in a result image. A progress item represents a segment of the result image.

To get this interface, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimageresult-get_progressitems">IFileSystemImageResult::get_ProgressItems</a> method.

## -inheritance

The <b>IProgressItems</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IProgressItems</b> also has these types of members:

## -remarks

This is a <b>ProgressItems</b> object in script.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems">IEnumProgressItems</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult">IFileSystemImageResult</a>

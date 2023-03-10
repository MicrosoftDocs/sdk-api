---
UID: NN:imapi2fs.IEnumProgressItems
title: IEnumProgressItems (imapi2fs.h)
description: Use this interface to enumerate a collection of progress items.
helpviewer_keywords: ["IEnumProgressItems","IEnumProgressItems interface [IMAPI]","IEnumProgressItems interface [IMAPI]","described","imapi.ienumprogressitems","imapi2fs/IEnumProgressItems"]
old-location: imapi\ienumprogressitems.htm
tech.root: imapi
ms.assetid: c4238fbe-762a-492f-9eb5-d927e64436e1
ms.date: 12/05/2018
ms.keywords: IEnumProgressItems, IEnumProgressItems interface [IMAPI], IEnumProgressItems interface [IMAPI],described, imapi.ienumprogressitems, imapi2fs/IEnumProgressItems
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
 - IEnumProgressItems
 - imapi2fs/IEnumProgressItems
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
 - IEnumProgressItems
---

# IEnumProgressItems interface


## -description

Use this interface to enumerate a collection of progress items.

To get this interface, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-iprogressitems-get_enumprogressitems">IProgressItems::get_EnumProgressItems</a> method.

## -inheritance

The <b>IEnumProgressItems</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumProgressItems</b> also has these types of members:

## -remarks

This is a <b>EnumProgressItems</b> object in script.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem">IProgressItem</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems">IProgressItems</a>

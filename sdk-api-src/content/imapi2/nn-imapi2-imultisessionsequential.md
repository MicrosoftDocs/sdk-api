---
UID: NN:imapi2.IMultisessionSequential
title: IMultisessionSequential (imapi2.h)
description: Use this interface to retrieve information about the previous import session on a sequentially recorded media, if the media contains a previous session.
helpviewer_keywords: ["IMultisessionSequential","IMultisessionSequential interface [IMAPI]","IMultisessionSequential interface [IMAPI]","described","imapi.imultisessionsequential","imapi2/IMultisessionSequential"]
old-location: imapi\imultisessionsequential.htm
tech.root: imapi
ms.assetid: b8124597-e75a-4f95-a25c-8cf59f452548
ms.date: 12/05/2018
ms.keywords: IMultisessionSequential, IMultisessionSequential interface [IMAPI], IMultisessionSequential interface [IMAPI],described, imapi.imultisessionsequential, imapi2/IMultisessionSequential
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IMultisessionSequential
 - imapi2/IMultisessionSequential
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
 - IMultisessionSequential
---

# IMultisessionSequential interface


## -description

Use this interface to retrieve information about the previous import session on a sequentially recorded media, if the media contains a previous session. 

The following methods return a collection of <a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a> interfaces representing all supported multisession types. <ul>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_multisessioninterfaces">IDiscFormat2Data::get_MultisessionInterfaces</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces">IFileSystemImage::get_MultisessionInterfaces</a>
</li>
</ul>The <b>IMultisession::QueryInterface</b> method can be called on each element in the collection to query for the <b>IMultisessionSequential</b> interface.

## -inheritance

The <b>IMultisessionSequential</b> interface inherits from <a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a>. <b>IMultisessionSequential</b> also has these types of members:

## -remarks

If more than one multi-session interface exist, the application can let <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a> choose a compatible multi-session interface to use  or the application can specify the multi-session interface to use by setting the <a href="/windows/desktop/api/imapi2/nf-imapi2-imultisession-put_inuse">put_InUse</a> property to VARIANT_TRUE.

A file system creator would use the address properties to import the content of the previous session on the disc and to compute the position of the next session it will create. These properties will return the same values as the properties of the same name of the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a> interface.

This is a <b>MsftMultisessionSequential</b> object in script.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a>

---
UID: NN:imapi2.IMultisessionRandomWrite
title: IMultisessionRandomWrite (imapi2.h)
description: Use this interface to retrieve information about the current state of media allowing random writes and not supporting the concept of physical sessions.
helpviewer_keywords: ["IMultisessionRandomWrite","IMultisessionRandomWrite interface [IMAPI]","IMultisessionRandomWrite interface [IMAPI]","described","imapi.imultisessionrandomwrite","imapi2/IMultisessionRandomWrite"]
old-location: imapi\imultisessionrandomwrite.htm
tech.root: imapi
ms.assetid: 1843254d-7947-4197-9c1b-6dc01abe9354
ms.date: 12/05/2018
ms.keywords: IMultisessionRandomWrite, IMultisessionRandomWrite interface [IMAPI], IMultisessionRandomWrite interface [IMAPI],described, imapi.imultisessionrandomwrite, imapi2/IMultisessionRandomWrite
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
 - IMultisessionRandomWrite
 - imapi2/IMultisessionRandomWrite
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
 - IMultisessionRandomWrite
---

# IMultisessionRandomWrite interface


## -description

Use this interface to retrieve information about the current state of media allowing random writes and not supporting the concept of physical sessions.

The following methods return a collection of <a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a> interfaces representing all supported multisession types. 
<ul>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_multisessioninterfaces">IDiscFormat2Data::get_MultisessionInterfaces</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces">IFileSystemImage::get_MultisessionInterfaces</a>
</li>
</ul>


You can then call the IUnknown::QueryInterface method on each element in the collection to query for the <b>IMultisessionRandomWrite</b> interface.

## -inheritance

The <b>IMultisessionRandomWrite</b> interface inherits from <a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a>. <b>IMultisessionRandomWrite</b> also has these types of members:

## -remarks

If more than one multi-session interface exist, the application can let <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a> choose a compatible multi-session interface to use or the application can specify the multi-session interface to use by setting the <i>put_InUse</i> property to <b>VARIANT_TRUE</b>.

A file system creator would use the address properties to import the content of the previous session on the disc and to compute the position of the next session it will create. These properties will return the same values as the properties of the same name of the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a> interface.
This is a <b>MsftMultisessionRandomWrite</b> object in script.

## -see-also

<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_multisessioninterfaces">IDiscFormat2Data::get_MultisessionInterfaces</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces">IFileSystemImage::get_MultisessionInterfaces</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a>

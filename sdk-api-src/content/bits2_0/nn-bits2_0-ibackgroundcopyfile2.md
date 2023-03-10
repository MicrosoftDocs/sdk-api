---
UID: NN:bits2_0.IBackgroundCopyFile2
title: IBackgroundCopyFile2 (bits2_0.h)
description: Use the IBackgroundCopyFile2 interface to specify a new remote name for the file and retrieve the list of ranges to download.
helpviewer_keywords: ["IBackgroundCopyFile2","IBackgroundCopyFile2 interface [BITS]","IBackgroundCopyFile2 interface [BITS]","described","bits.ibackgroundcopyfile2","bits2_0/IBackgroundCopyFile2"]
old-location: bits\ibackgroundcopyfile2.htm
tech.root: Bits
ms.assetid: facff24d-56a3-4a1f-a726-3442c17fe869
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyFile2, IBackgroundCopyFile2 interface [BITS], IBackgroundCopyFile2 interface [BITS],described, bits.ibackgroundcopyfile2, bits2_0/IBackgroundCopyFile2
req.header: bits2_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2,KB842773 on  Windows Server 2003, and  Windows XP
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits2_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: BitsPrx3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyFile2
 - bits2_0/IBackgroundCopyFile2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx3.dll
api_name:
 - IBackgroundCopyFile2
---

# IBackgroundCopyFile2 interface


## -description

Use the 
<b>IBackgroundCopyFile2</b> interface to specify a new remote name  for the file and retrieve the list of ranges to download.

The 
<b>IBackgroundCopyFile2</b> interface inherits from the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a> interface. 

To get an 
<b>IBackgroundCopyFile2</b> interface pointer, call the <b>IBackgroundCopyFile::QueryInterface</b> method using __uuidof(IBackgroundCopyFile2) for the interface identifier. Use the 
<b>IBackgroundCopyFile2</b> interface pointer to call both the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a> and 
<b>IBackgroundCopyFile2</b> methods.

## -inheritance

The <b>IBackgroundCopyFile2</b> interface inherits from <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a>. <b>IBackgroundCopyFile2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a>

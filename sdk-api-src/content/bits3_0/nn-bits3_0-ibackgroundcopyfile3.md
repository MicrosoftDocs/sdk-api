---
UID: NN:bits3_0.IBackgroundCopyFile3
title: IBackgroundCopyFile3 (bits3_0.h)
description: Use this interface to retrieve the name of the temporary file that contains the downloaded content and to validate the file so that peers can request its content.
helpviewer_keywords: ["IBackgroundCopyFile3","IBackgroundCopyFile3 interface [BITS]","IBackgroundCopyFile3 interface [BITS]","described","bits.ibackgroundcopyfile3","bits3_0/IBackgroundCopyFile3"]
old-location: bits\ibackgroundcopyfile3.htm
tech.root: Bits
ms.assetid: 5304f93a-993a-4327-9fdb-fb2ef1dafecb
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyFile3, IBackgroundCopyFile3 interface [BITS], IBackgroundCopyFile3 interface [BITS],described, bits.ibackgroundcopyfile3, bits3_0/IBackgroundCopyFile3
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyFile3
 - bits3_0/IBackgroundCopyFile3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyFile3
---

# IBackgroundCopyFile3 interface


## -description

Use this 
interface to retrieve the name of the temporary file that contains the downloaded content and to validate the file so that peers can request its content.

To get an 
<b>IBackgroundCopyFile3</b> interface pointer, call the <b>IBackgroundCopyFile::QueryInterface</b> method using __uuidof(IBackgroundCopyFile3) for the interface identifier.

## -inheritance

The <b>IBackgroundCopyFile3</b> interface inherits from <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a> and <a href="/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyfile2">IBackgroundCopyFile2</a>. <b>IBackgroundCopyFile3</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a>



<a href="/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyfile2">IBackgroundCopyFile2</a>

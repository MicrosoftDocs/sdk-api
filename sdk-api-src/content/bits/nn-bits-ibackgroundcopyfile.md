---
UID: NN:bits.IBackgroundCopyFile
title: IBackgroundCopyFile (bits.h)
description: IBackgroundCopyFile contains information about a file that is part of a job. For example, you can use IBackgroundCopyFile methods to retrieve the local and remote names of the file and transfer progress information.
helpviewer_keywords: ["IBackgroundCopyFile","IBackgroundCopyFile interface [BITS]","IBackgroundCopyFile interface [BITS]","described","_drz_ibackgroundcopyfile","bits.ibackgroundcopyfile","bits/IBackgroundCopyFile"]
old-location: bits\ibackgroundcopyfile.htm
tech.root: Bits
ms.assetid: fae9cf56-c211-445b-b962-9a9d7d67c59c
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyFile, IBackgroundCopyFile interface [BITS], IBackgroundCopyFile interface [BITS],described, _drz_ibackgroundcopyfile, bits.ibackgroundcopyfile, bits/IBackgroundCopyFile
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyFile
 - bits/IBackgroundCopyFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyFile
---

# IBackgroundCopyFile interface


## -description

<b>IBackgroundCopyFile</b> contains information about a file that is part of a job. For example, you can use <b>IBackgroundCopyFile</b> methods to retrieve the local and remote names of the file and transfer progress information.

To get an 
<b>IBackgroundCopyFile</b> interface pointer, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-getfile">IBackgroundCopyError::GetFile</a> method or the 
<a href="/windows/desktop/api/bits/nf-bits-ienumbackgroundcopyfiles-next">IEnumBackgroundCopyFiles::Next</a> method.

## -inheritance

The <b>IBackgroundCopyFile</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBackgroundCopyFile</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyerror">IBackgroundCopyError</a>



<a href="/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyfile2">IBackgroundCopyFile2</a>



<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>



<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyfiles">IEnumBackgroundCopyFiles</a>

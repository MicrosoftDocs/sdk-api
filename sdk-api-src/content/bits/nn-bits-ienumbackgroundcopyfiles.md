---
UID: NN:bits.IEnumBackgroundCopyFiles
title: IEnumBackgroundCopyFiles (bits.h)
description: Use the IEnumBackgroundCopyFiles interface to enumerate the files that a job contains. To get an IEnumBackgroundCopyFiles interface pointer, call the IBackgroundCopyJob::EnumFiles method.
helpviewer_keywords: ["IEnumBackgroundCopyFiles","IEnumBackgroundCopyFiles interface [BITS]","IEnumBackgroundCopyFiles interface [BITS]","described","_drz_ienumbackgroundcopyfiles","bits.ienumbackgroundcopyfiles","bits/IEnumBackgroundCopyFiles"]
old-location: bits\ienumbackgroundcopyfiles.htm
tech.root: Bits
ms.assetid: 831998ba-601c-43c4-ba27-faff741f8eb4
ms.date: 12/05/2018
ms.keywords: IEnumBackgroundCopyFiles, IEnumBackgroundCopyFiles interface [BITS], IEnumBackgroundCopyFiles interface [BITS],described, _drz_ienumbackgroundcopyfiles, bits.ienumbackgroundcopyfiles, bits/IEnumBackgroundCopyFiles
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
 - IEnumBackgroundCopyFiles
 - bits/IEnumBackgroundCopyFiles
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
 - IEnumBackgroundCopyFiles
---

# IEnumBackgroundCopyFiles interface


## -description

Use the 
<b>IEnumBackgroundCopyFiles</b> interface to enumerate the files that a job contains. To get an 
<b>IEnumBackgroundCopyFiles</b> interface pointer, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-enumfiles">IBackgroundCopyJob::EnumFiles</a> method.

## -inheritance

The <b>IEnumBackgroundCopyFiles</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumBackgroundCopyFiles</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-enumfiles">IBackgroundCopyJob::EnumFiles</a>



<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyjobs">IEnumBackgroundCopyJobs</a>

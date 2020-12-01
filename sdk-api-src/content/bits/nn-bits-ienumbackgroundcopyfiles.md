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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumBackgroundCopyFiles</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumBackgroundCopyFiles</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumBackgroundCopyFiles</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bits/nf-bits-ienumbackgroundcopyfiles-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bits/nf-bits-ienumbackgroundcopyfiles-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bits/nf-bits-ienumbackgroundcopyfiles-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bits/nf-bits-ienumbackgroundcopyfiles-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bits/nf-bits-ienumbackgroundcopyfiles-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of items in the enumeration sequence.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-enumfiles">IBackgroundCopyJob::EnumFiles</a>



<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyjobs">IEnumBackgroundCopyJobs</a>
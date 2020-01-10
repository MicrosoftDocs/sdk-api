---
UID: NN:bits.IBackgroundCopyFile
title: IBackgroundCopyFile (bits.h)
description: IBackgroundCopyFile contains information about a file that is part of a job. For example, you can use IBackgroundCopyFile methods to retrieve the local and remote names of the file and transfer progress information.
old-location: bits\ibackgroundcopyfile.htm
tech.root: Bits
ms.assetid: fae9cf56-c211-445b-b962-9a9d7d67c59c
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyFile, IBackgroundCopyFile interface [BITS], IBackgroundCopyFile interface [BITS],described, _drz_ibackgroundcopyfile, bits.ibackgroundcopyfile, bits/IBackgroundCopyFile
f1_keywords:
- bits/IBackgroundCopyFile
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- QmgrPrxy.dll
api_name:
- IBackgroundCopyFile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBackgroundCopyFile interface


## -description


<b>IBackgroundCopyFile</b> contains information about a file that is part of a job. For example, you can use <b>IBackgroundCopyFile</b> methods to retrieve the local and remote names of the file and transfer progress information.

To get an 
<b>IBackgroundCopyFile</b> interface pointer, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-getfile">IBackgroundCopyError::GetFile</a> method or the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ienumbackgroundcopyfiles-next">IEnumBackgroundCopyFiles::Next</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyFile</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBackgroundCopyFile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyFile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyfile-getlocalname">GetLocalName</a>
</td>
<td align="left" width="63%">
Retrieves the local name of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyfile-getprogress">GetProgress</a>
</td>
<td align="left" width="63%">
Retrieves the progress of the file transfer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nf-bits-ibackgroundcopyfile-getremotename">GetRemoteName</a>
</td>
<td align="left" width="63%">
Retrieves the remote name of the file.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyerror">IBackgroundCopyError</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyfile2">IBackgroundCopyFile2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyfiles">IEnumBackgroundCopyFiles</a>
 

 


---
UID: NN:bits3_0.IBackgroundCopyFile3
title: IBackgroundCopyFile3 (bits3_0.h)
author: windows-sdk-content
description: Use this interface to retrieve the name of the temporary file that contains the downloaded content and to validate the file so that peers can request its content.
old-location: bits\ibackgroundcopyfile3.htm
tech.root: Bits
ms.assetid: 5304f93a-993a-4327-9fdb-fb2ef1dafecb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyFile3, IBackgroundCopyFile3 interface [BITS], IBackgroundCopyFile3 interface [BITS],described, bits.ibackgroundcopyfile3, bits3_0/IBackgroundCopyFile3
ms.topic: interface
f1_keywords: ["bits3_0/IBackgroundCopyFile3"]
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBackgroundCopyFile3 interface


## -description


Use this 
interface to retrieve the name of the temporary file that contains the downloaded content and to validate the file so that peers can request its content.

To get an 
<b>IBackgroundCopyFile3</b> interface pointer, call the <b>IBackgroundCopyFile::QueryInterface</b> method using __uuidof(IBackgroundCopyFile3) for the interface identifier. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyFile3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a> and <a href="https://docs.microsoft.com/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyfile2">IBackgroundCopyFile2</a>. <b>IBackgroundCopyFile3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyFile3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname">GetTemporaryName</a>
</td>
<td align="left" width="63%">
Gets the full path of the temporary file that contains the content of the download.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyfile3-getvalidationstate">GetValidationState</a>
</td>
<td align="left" width="63%">
Gets the validation state of this file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyfile3-isdownloadedfrompeer">IsDownloadedFromPeer</a>
</td>
<td align="left" width="63%">
Gets a value that determines if any part of the file was downloaded from a peer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate">SetValidationState</a>
</td>
<td align="left" width="63%">
Sets the validation state of this file.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyfile2">IBackgroundCopyFile2</a>
 

 


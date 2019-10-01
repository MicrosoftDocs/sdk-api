---
UID: NN:bits5_0.IBackgroundCopyFile5
title: IBackgroundCopyFile5 (bits5_0.h)
author: windows-sdk-content
description: Use this interface to get or set generic properties of BITS file transfers.
old-location: bits\ibackgroundcopyfile5.htm
tech.root: Bits
ms.assetid: 548b507a-4874-4ccf-829e-13e1ca6cc958
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyFile5, IBackgroundCopyFile5 interface [BITS], IBackgroundCopyFile5 interface [BITS],described, bits.ibackgroundcopyfile5, bits5_0/IBackgroundCopyFile5
ms.topic: interface
f1_keywords: 
 - "bits5_0/IBackgroundCopyFile5"
req.header: bits5_0.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits5_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits5_0.h
api_name:
 - IBackgroundCopyFile5
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBackgroundCopyFile5 interface


## -description


Use this 
interface to get or set generic properties of BITS file transfers.

To get an 
<b>IBackgroundCopyFile5</b> interface pointer, call the <b>IBackgroundCopyFile::QueryInterface</b> method using __uuidof(IBackgroundCopyFile5) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyFile5</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/bits4_0/nn-bits4_0-ibackgroundcopyfile4">IBackgroundCopyFile4</a>. <b>IBackgroundCopyFile5</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyFile5</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits5_0/nf-bits5_0-ibackgroundcopyfile5-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Gets the value of a generic BackgroundCopyFile property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits5_0/nf-bits5_0-ibackgroundcopyfile5-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the value of a generic BackgroundCopyFile property.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyfile2">IBackgroundCopyFile2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nn-bits3_0-ibackgroundcopyfile3">IBackgroundCopyFile3</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits4_0/nn-bits4_0-ibackgroundcopyfile4">IBackgroundCopyFile4</a>
 

 


---
UID: NN:msrdc.IRdcFileReader
title: IRdcFileReader (msrdc.h)
description: The IRdcFileReader interface is used to provide the equivalent of a file handle, because the data being synchronized may not exist as a file on disk.
old-location: rdc\irdcfilereader.htm
tech.root: rdc
ms.assetid: 9684efca-37fd-45ce-a24e-d5276b8ea6af
ms.date: 12/05/2018
ms.keywords: IRdcFileReader, IRdcFileReader interface [Remote Differential Compression], IRdcFileReader interface [Remote Differential Compression],described, fs.irdcfilereader, msrdc/IRdcFileReader, rdc.irdcfilereader
ms.topic: interface
f1_keywords:
- msrdc/IRdcFileReader
dev_langs:
- c++
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: MsRdc.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- MsRdc.dll
api_name:
- IRdcFileReader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRdcFileReader interface


## -description


The <b>IRdcFileReader</b> interface is used to provide the 
    equivalent of a file handle, because the data being synchronized may not exist as a file on disk.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcFileReader</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRdcFileReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRdcFileReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcfilereader-getfileposition">GetFilePosition</a>
</td>
<td align="left" width="63%">
Returns the current file position.</p> (Inherited from <b>IRdcFileReader</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcfilereader-getfilesize">GetFileSize</a>
</td>
<td align="left" width="63%">
Returns the 
    size of a file.</p> (Inherited from <b>IRdcFileReader</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcfilereader-read">Read</a>
</td>
<td align="left" width="63%">
Reads the specified amount 
    of data starting at the specified position.</p> (Inherited from <b>IRdcFileReader</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdclibrary-createcomparator">IRdcLibrary::CreateComparator</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdclibrary-createsignaturereader">IRdcLibrary::CreateSignatureReader</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/rdc/remote-differential-compression-interfaces">Remote Differential Compression Interfaces</a>
 

 


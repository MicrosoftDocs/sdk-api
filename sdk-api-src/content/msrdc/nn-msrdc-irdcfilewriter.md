---
UID: NN:msrdc.IRdcFileWriter
title: IRdcFileWriter (msrdc.h)
author: windows-sdk-content
description: Abstract interface to read from and write to a file.
old-location: rdc\irdcfilewriter.htm
tech.root: rdc
ms.assetid: 8b6ac8d0-37fd-4bd3-aa44-5b57f546364d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRdcFileWriter, IRdcFileWriter interface [Remote Differential Compression], IRdcFileWriter interface [Remote Differential Compression],described, fs.irdcfilewriter, msrdc/IRdcFileWriter, rdc.irdcfilewriter
ms.topic: interface
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
 - IRdcFileWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRdcFileWriter interface


## -description


Abstract interface to read from and write to a file.

The RDC application must implement this interface for use with <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarityfileidtable-createtableindirect">ISimilarityFileIdTable::CreateTableIndirect</a>. Note that this interface does not include methods to open, close, or flush the file to disk. The application is responsible for properly opening and closing the file represented by an instance of this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcFileWriter</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilereader">IRdcFileReader</a>. <b>IRdcFileWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRdcFileWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcfilewriter-deleteonclose">DeleteOnClose</a>
</td>
<td align="left" width="63%">
Sets a file to be deleted (or truncated) on close.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcfilewriter-truncate">Truncate</a>
</td>
<td align="left" width="63%">
Truncates a file to zero length.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcfilewriter-write">Write</a>
</td>
<td align="left" width="63%">
Write bytes to a file starting at a given offset.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilereader">IRdcFileReader</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 


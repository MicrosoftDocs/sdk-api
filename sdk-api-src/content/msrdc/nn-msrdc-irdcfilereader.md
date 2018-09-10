---
UID: NN:msrdc.IRdcFileReader
title: IRdcFileReader
author: windows-sdk-content
description: The IRdcFileReader interface is used to provide the equivalent of a file handle, because the data being synchronized may not exist as a file on disk.
old-location: rdc\irdcfilereader.htm
tech.root: Rdc
ms.assetid: 9684efca-37fd-45ce-a24e-d5276b8ea6af
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IRdcFileReader, IRdcFileReader interface [Remote Differential Compression], IRdcFileReader interface [Remote Differential Compression],described, fs.irdcfilereader, msrdc/IRdcFileReader, rdc.irdcfilereader
ms.prod: windows
ms.technology: windows-sdk
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
 - IRdcFileReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRdcFileReader interface


## -description


The <b>IRdcFileReader</b> interface is used to provide the 
    equivalent of a file handle, because the data being synchronized may not exist as a file on disk.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcFileReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRdcFileReader</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3cef6883-29d2-4970-9a96-3500b58449d2">GetFilePosition</a>
</td>
<td align="left" width="63%">
Returns the current file position.</p> (Inherited from <b>IRdcFileReader</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2db66eb0-7213-446a-ad4b-f0df9e48abd4">GetFileSize</a>
</td>
<td align="left" width="63%">
Returns the 
    size of a file.</p> (Inherited from <b>IRdcFileReader</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/194944c8-94a8-4f9b-9970-012392e069b1">Read</a>
</td>
<td align="left" width="63%">
Reads the specified amount 
    of data starting at the specified position.</p> (Inherited from <b>IRdcFileReader</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/21e83ed0-974a-470f-8a7f-1776f1575100">IRdcLibrary::CreateComparator</a>



<a href="https://msdn.microsoft.com/08627c9d-7470-47ab-9209-32734082c393">IRdcLibrary::CreateSignatureReader</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/a3131654-e849-4a88-acec-c49a61653bad">Remote Differential Compression Interfaces</a>
 

 


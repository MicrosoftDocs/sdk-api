---
UID: NN:msrdc.IRdcFileWriter
title: IRdcFileWriter
author: windows-sdk-content
description: Abstract interface to read from and write to a file.
old-location: rdc\irdcfilewriter.htm
tech.root: rdc
ms.assetid: 8b6ac8d0-37fd-4bd3-aa44-5b57f546364d
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IRdcFileWriter, IRdcFileWriter interface [Remote Differential Compression], IRdcFileWriter interface [Remote Differential Compression],described, fs.irdcfilewriter, msrdc/IRdcFileWriter, rdc.irdcfilewriter
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# IRdcFileWriter interface


## -description


Abstract interface to read from and write to a file.

The RDC application must implement this interface for use with <a href="https://msdn.microsoft.com/6e472ab0-efa4-4edd-8d78-68d5a66cf41c">ISimilarityFileIdTable::CreateTableIndirect</a>. Note that this interface does not include methods to open, close, or flush the file to disk. The application is responsible for properly opening and closing the file represented by an instance of this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcFileWriter</b> interface inherits from <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> and <a href="https://msdn.microsoft.com/9684efca-37fd-45ce-a24e-d5276b8ea6af">IRdcFileReader</a>. <b>IRdcFileWriter</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/188d43b7-db97-479e-8d4c-e7826d5c3952">DeleteOnClose</a>
</td>
<td align="left" width="63%">
Sets a file to be deleted (or truncated) on close.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71a9a573-a354-47ce-89a0-ebc5acd86159">Truncate</a>
</td>
<td align="left" width="63%">
Truncates a file to zero length.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be7f3f2c-017a-4ca5-9652-a9b091c168be">Write</a>
</td>
<td align="left" width="63%">
Write bytes to a file starting at a given offset.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9684efca-37fd-45ce-a24e-d5276b8ea6af">IRdcFileReader</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 


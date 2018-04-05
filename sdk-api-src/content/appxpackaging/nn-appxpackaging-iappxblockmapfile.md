---
UID: NN:appxpackaging.IAppxBlockMapFile
title: IAppxBlockMapFile
author: windows-driver-content
description: Represents a file in the block map.
old-location: appxpkg\iappxblockmapfile.htm
old-project: appxpkg
ms.assetid: 4C380E2F-8125-4147-97F5-BEDF5BEFB81D
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: IAppxBlockMapFile, IAppxBlockMapFile interface [App packaging and management], IAppxBlockMapFile interface [App packaging and management], described, appxpackaging/IAppxBlockMapFile, appxpkg.iappxblockmapfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: APPX_PACKAGE_ARCHITECTURE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxBlockMapFile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBlockMapFile interface


## -description


Represents a file in the block map.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBlockMapFile</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBlockMapFile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBlockMapFile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CE8FB813-B125-4FD6-A7C3-CA3ECA72ECE7">GetBlocks</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for traversing the blocks of a file listed in the block map.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2BBABACF-089B-4711-B384-627E921B044A">GetLocalFileHeaderSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the zip local file header of the associated zip file item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82D100DB-CAE8-4FF7-B428-B14E8CBDE7A5">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the associated zip file item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35D3EADC-F8EF-4D8F-8016-2E30976965EC">GetUncompressedSize</a>
</td>
<td align="left" width="63%">
Retrieves the uncompressed size of the associated zip file item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/286EF8FD-925E-4B36-AFAB-D0EC949F8705">ValidateFileHash</a>
</td>
<td align="left" width="63%">
Validates the content of a file against the hashes stored in the block elements for this block map file.

</td>
</tr>
</table> 


## -remarks



The <b>IAppxBlockMapFile</b> interface provides a read-only object model that represents the files in the block map. Files are represented in the block map file with the <b>File</b> element. You can retrieve the file's attributes and block hashes from the <b>File</b> element. Block hashes can be obtained from the <a href="https://msdn.microsoft.com/39B0680A-F27B-478F-8E83-FE1BFCF61AC4">IAppxBlockMapBlock</a> interface.


#### Examples

For a example code, see <a href="http://go.microsoft.com/fwlink/p/?linkid=236966">Read app package manifest info sample (DescribeAppx)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/39B0680A-F27B-478F-8E83-FE1BFCF61AC4">IAppxBlockMapBlock</a>



<a href="https://msdn.microsoft.com/E7678755-4779-4A64-A666-C5FFC4A7F37A">IAppxBlockMapBlocksEnumerator</a>



<a href="https://msdn.microsoft.com/AC2E55C3-1EEF-4867-BECC-37F6269029D6">IAppxBlockMapFilesEnumerator</a>



<a href="https://msdn.microsoft.com/233539FD-E3BE-4783-9F23-B34F6397FBBE">IAppxBlockMapReader</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=236966">Read app package manifest info sample (DescribeAppx)</a>



<b>Reference</b>



<b>Samples</b>
 

 


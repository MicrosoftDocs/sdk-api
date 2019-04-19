---
UID: NN:appxpackaging.IAppxBlockMapReader
title: IAppxBlockMapReader (appxpackaging.h)
author: windows-sdk-content
description: Represents a read-only object model for block maps that provides access to the file attributes and block hashes.
old-location: appxpkg\iappxblockmapreader.htm
tech.root: appxpkg
ms.assetid: 233539FD-E3BE-4783-9F23-B34F6397FBBE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxBlockMapReader, IAppxBlockMapReader interface [App packaging and management], IAppxBlockMapReader interface [App packaging and management],described, appxpackaging/IAppxBlockMapReader, appxpkg.iappxblockmapreader
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxBlockMapReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBlockMapReader interface


## -description


Represents a read-only object model for block maps that provides access to the file attributes and block hashes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBlockMapReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBlockMapReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBlockMapReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3F38BC3A-9CFD-4FB3-A744-612E25DF0F0F">GetFile</a>
</td>
<td align="left" width="63%">
Retrieves data corresponding to a file in the block map with the specified file name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7E46C555-8C61-4F26-9732-07E0DEEAF66F">GetFiles</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for traversing the files listed in the block map.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/661E4F12-E426-4811-81FA-4F065C6E488A">GetHashMethod</a>
</td>
<td align="left" width="63%">
Retrieves the URI for the hash algorithm used to create block hashes in the block map.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95EBABDA-45D5-436C-B627-51C14D9091EA">GetStream</a>
</td>
<td align="left" width="63%">
Retrieves a read-only stream that represents the XML content of the block map.

</td>
</tr>
</table> 


## -remarks



The <b>IAppxBlockMapReader</b> represents the <b>BlockMap</b> root element of the block map. <b>File</b> elements are the child elements of the <b>BlockMap</b> element.

This object can be retrieved using the <a href="https://msdn.microsoft.com/B4A310F0-4276-49AA-9ABF-A98F41E8F87F">CreateBlockMapReader</a> or <a href="https://msdn.microsoft.com/BCC39D9C-4AF9-4CFD-AC66-4B79F9F25BDC">CreateValidatedBlockMapReader</a> method of the <a href="https://msdn.microsoft.com/4EA79D44-7C26-4B65-81A1-394E1E540F34">IAppxFactory</a> interface, or the <a href="https://msdn.microsoft.com/FEBCA2E4-9B32-499B-AD31-9D90525A42DB">GetBlockMap </a>method of the <a href="https://msdn.microsoft.com/D34D0909-BE2B-4182-8C3D-36A4E8DDC820">IAppxPackageReader</a> interface.


#### Examples

For a example code, see <a href="http://go.microsoft.com/fwlink/p/?linkid=236966">Read app package manifest info sample (DescribeAppx)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/39B0680A-F27B-478F-8E83-FE1BFCF61AC4">IAppxBlockMapBlock</a>



<a href="https://msdn.microsoft.com/E7678755-4779-4A64-A666-C5FFC4A7F37A">IAppxBlockMapBlocksEnumerator</a>



<a href="https://msdn.microsoft.com/4C380E2F-8125-4147-97F5-BEDF5BEFB81D">IAppxBlockMapFile</a>



<a href="https://msdn.microsoft.com/AC2E55C3-1EEF-4867-BECC-37F6269029D6">IAppxBlockMapFilesEnumerator</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=236966">Read app package manifest info sample (DescribeAppx)</a>



<b>Reference</b>



<b>Samples</b>
 

 


---
UID: NN:wmsdkidl.IWMIndexer
title: IWMIndexer (wmsdkidl.h)
author: windows-sdk-content
description: The IWMIndexer interface is used to create an index for ASF files to enable seeking.
old-location: wmformat\iwmindexer.htm
tech.root: wmformat
ms.assetid: 00627b0c-4484-417a-8680-0fd97aac41fe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMIndexer, IWMIndexer interface [windows Media Format], IWMIndexer interface [windows Media Format],described, IWMIndexerInterface, wmformat.iwmindexer, wmsdkidl/IWMIndexer
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMIndexer"
dev_langs:
 - c++
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - wmsdkidl.h
api_name:
 - IWMIndexer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMIndexer interface


## -description



The <b>IWMIndexer</b> interface is used to create an index for ASF files to enable seeking. An index is created only for a file that contains video, although the indexer can safely be used on files that do not contain any video.

An index is an object in the ASF file that equates video samples with presentation times. This is important because the timing of video frames is not necessarily easily computed from the <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">frame rate</a>.

In addition to the standard temporal index, the indexer object can create indexes based on video frame number and SMPTE time code. For more information about creating these indexes, see <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmindexer2-configure">IWMIndexer2::Configure</a>.

This interface can be obtained by using the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreateindexer">WMCreateIndexer</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMIndexer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMIndexer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMIndexer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmindexer-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing">StartIndexing</a>
</td>
<td align="left" width="63%">
Initiates indexing.

</td>
</tr>
</table> 

The following interface can be obtained by using the QueryInterface method of this interface.

<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2">IWMIndexer2</a>
</td>
<td>IID_IWMIndexer2</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/indexer-object">Indexer Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 


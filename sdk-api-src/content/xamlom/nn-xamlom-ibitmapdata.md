---
UID: NN:xamlom.IBitmapData
title: IBitmapData (xamlom.h)

description: Represents an image associated with a node in the visual tree.
old-location: xaml_diagnostics\ibitmapdata.htm
tech.root: xaml_diagnostics
ms.assetid: 5B833E2A-D150-4ECA-88C8-CEEDBF2E23C6

ms.date: 12/05/2018
ms.keywords: IBitmapData, IBitmapData interface, IBitmapData interface,described, xaml_diagnostics.ibitmapdata, xamlom/IBitmapData
ms.topic: interface
f1_keywords: 
 - "xamlom/IBitmapData"
dev_langs:
 - c++
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
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
 - xamlom.h
api_name:
 - IBitmapData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBitmapData interface


## -description


Represents an image associated with a node in the visual tree.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBitmapData</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBitmapData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBitmapData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ibitmapdata-copybytesto">CopyBytesTo</a>
</td>
<td align="left" width="63%">
Copies up to the specified maximum number of bytes from the given offset in the bitmap data into the caller’s buffer (<i>pvBytes</i>), and returns the number of bytes copied.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ibitmapdata-getbitmapdescription">GetBitmapDescription</a>
</td>
<td align="left" width="63%">
Gets a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/ns-xamlom-bitmapdescription">BitmapDescription</a> that describes the bitmap data stored in the <b>IBitmapData</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ibitmapdata-getsourcebitmapdescription">GetSourceBitmapDescription</a>
</td>
<td align="left" width="63%">
Gets a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/ns-xamlom-bitmapdescription">BitmapDescription</a> that describes the original format of the bitmap data stored in the <b>IBitmapData</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ibitmapdata-getstride">GetStride</a>
</td>
<td align="left" width="63%">
Gets the stride of the data. This is the length in bytes of each row of the bitmap. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 


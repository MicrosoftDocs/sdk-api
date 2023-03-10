---
UID: NL:vswriter.IVssCreateWriterMetadataEx
title: IVssCreateWriterMetadataEx (vswriter.h)
description: The IVssCreateWriterMetadataEx interface is a C++ (not COM) interface that defines a method to report any file sets that will be explicitly excluded when a shadow copy is created.
helpviewer_keywords: ["IVssCreateWriterMetadataEx","IVssCreateWriterMetadataEx interface","IVssCreateWriterMetadataEx interface","described","base.ivsscreatewritermetadataex","vswriter/IVssCreateWriterMetadataEx"]
old-location: base\ivsscreatewritermetadataex.htm
tech.root: base
ms.assetid: eec0a7ef-ad7c-4fb6-a101-573c2d0943c2
ms.date: 12/05/2018
ms.keywords: IVssCreateWriterMetadataEx, IVssCreateWriterMetadataEx interface, IVssCreateWriterMetadataEx interface,described, base.ivsscreatewritermetadataex, vswriter/IVssCreateWriterMetadataEx
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssCreateWriterMetadataEx
 - vswriter/IVssCreateWriterMetadataEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssCreateWriterMetadataEx
---

# IVssCreateWriterMetadataEx class


## -description

The 
<b>IVssCreateWriterMetadataEx</b> interface is a C++ (not COM) interface that defines a method to report any <a href="/windows/desktop/VSS/vssgloss-f">file sets</a> that will be explicitly excluded when a shadow copy is created. This interface is used only in 
the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onidentify">CVssWriterEx::OnIdentifyEx</a> method.

The <b>IVssCreateWriterMetadataEx</b> interface inherits from the <a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a> interface and <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>.

<b>IVssCreateWriterMetadataEx</b> defines the following method.<table>
<tr>
<th>Method</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot">AddExcludeFilesFromSnapshot</a>
</td>
<td>Reports any <a href="/windows/desktop/VSS/vssgloss-f">file sets</a> that will be explicitly excluded by the writer when a shadow copy is created.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a>
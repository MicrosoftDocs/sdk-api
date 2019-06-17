---
UID: NL:vswriter.IVssExpressWriter
title: IVssExpressWriter (vswriter.h)
author: windows-sdk-content
description: Defines methods to manage metadata for a VSS express writer.
old-location: base\ivssexpresswriter.htm
tech.root: VSS
ms.assetid: debb0731-6e24-4320-8236-220e07ec37c3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVssExpressWriter, IVssExpressWriter interface, IVssExpressWriter interface,described, base.ivssexpresswriter, vswriter/IVssExpressWriter
ms.topic: class
f1_keywords: ["vswriter/IVssExpressWriter"]
req.header: vswriter.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - VsWriter.h
api_name:
 - IVssExpressWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssExpressWriter class


## -description


Defines methods to manage metadata for a VSS express writer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssExpressWriter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssExpressWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssExpressWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivssexpresswriter-createmetadata">CreateMetadata</a>
</td>
<td align="left" width="63%">
Creates an express writer metadata object and returns an <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivsscreateexpresswritermetadata">IVssCreateExpressWriterMetadata</a> interface pointer to it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivssexpresswriter-loadmetadata">LoadMetadata</a>
</td>
<td align="left" width="63%">
Causes VSS to load the writer's metadata from a string instead of the express writer metadata store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivssexpresswriter-register">Register</a>
</td>
<td align="left" width="63%">
Causes VSS to store the writer's metadata in the express writer metadata store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivssexpresswriter-unregister">Unregister</a>
</td>
<td align="left" width="63%">
Causes VSS to delete the writer's metadata from the express writer metadata store.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-createvssexpresswriter">CreateVssExpressWriter</a>
 

 


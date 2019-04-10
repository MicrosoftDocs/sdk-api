---
UID: NN:msctf.ITfTransitoryExtensionUIElement
title: ITfTransitoryExtensionUIElement (msctf.h)
author: windows-sdk-content
description: The ITfTransitoryExtensionUIElement interface is implemented by TSF manager which provides the UI of transitory extension.
old-location: tsf\itftransitoryextensionuielement.htm
tech.root: TSF
ms.assetid: 37fd507b-6c06-4873-b8b4-11113edb1433
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfTransitoryExtensionUIElement, ITfTransitoryExtensionUIElement interface [Text Services Framework], ITfTransitoryExtensionUIElement interface [Text Services Framework],described, _tsf_itftransitoryextensionuielement_ref, msctf/ITfTransitoryExtensionUIElement, tsf.itftransitoryextensionuielement
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - Msctf.h
api_name:
 - ITfTransitoryExtensionUIElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfTransitoryExtensionUIElement interface


## -description


The <b>ITfTransitoryExtensionUIElement</b> interface is implemented by TSF manager which provides the UI of transitory extension. The application that is in UILess mode will use this interface to determine if the original UI should be shown or the content of this UI should be drown by the application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfTransitoryExtensionUIElement</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfTransitoryExtensionUIElement</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfTransitoryExtensionUIElement</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/199598fc-09e8-4d3b-b460-c76a1e4ee623">GetDocumentMgr</a>
</td>
<td align="left" width="63%">
Returns the pointer of the transitory document manager.

</td>
</tr>
</table> 


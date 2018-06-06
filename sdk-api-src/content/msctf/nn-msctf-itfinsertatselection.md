---
UID: NN:msctf.ITfInsertAtSelection
title: ITfInsertAtSelection
author: windows-sdk-content
description: The ITfInsertAtSelection interface is implemented by the manager and is used by a text service to insert text or an embedded object in a context. The text service obtains this interface by calling ITfContext::QueryInterface.
old-location: tsf\itfinsertatselection.htm
old-project: TSF
ms.assetid: bd303639-942f-4cb0-8d69-1715f85b6ef3
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfInsertAtSelection, ITfInsertAtSelection interface [Text Services Framework], ITfInsertAtSelection interface [Text Services Framework],described, _tsf_itfinsertatselection_ref, msctf/ITfInsertAtSelection, tsf.itfinsertatselection
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfInsertAtSelection
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfInsertAtSelection interface


## -description


The <b>ITfInsertAtSelection</b> interface is implemented by the manager and is used by a text service to insert text or an embedded object in a context. The text service obtains this interface by calling ITfContext::QueryInterface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfInsertAtSelection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfInsertAtSelection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfInsertAtSelection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13fa9955-0087-4dd9-8a1d-814ab801e956">InsertEmbeddedAtSelection</a>
</td>
<td align="left" width="63%">
Inserts an IDataObject object at the selection or insertion point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1373fe9b-6c51-4514-a7da-c1f872d9b1ce">InsertTextAtSelection</a>
</td>
<td align="left" width="63%">
Inserts text at the selection or insertion point.

</td>
</tr>
</table> 


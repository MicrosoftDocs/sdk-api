---
UID: NF:textstor.ITextStoreACPSink.OnSelectionChange
title: ITextStoreACPSink::OnSelectionChange method
author: windows-driver-content
description: ITextStoreACPSink::OnSelectionChange method
old-location: tsf\itextstoreacpsink_onselectionchange.htm
old-project: TSF
ms.assetid: 500333ae-06dc-4194-a21b-e03c1acc9f9a
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITextStoreACPSink, ITextStoreACPSink interface [Text Services Framework], OnSelectionChange method, ITextStoreACPSink::OnSelectionChange, OnSelectionChange method [Text Services Framework], OnSelectionChange method [Text Services Framework], ITextStoreACPSink interface, OnSelectionChange,ITextStoreACPSink.OnSelectionChange, _tsf_itextstoreacpsink_onselectionchange_ref, textstor/ITextStoreACPSink::OnSelectionChange, tsf.itextstoreacpsink_onselectionchange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITextStoreACPSink.OnSelectionChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACPSink::OnSelectionChange method


## -description




## -parameters






## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The manager holds a lock on the document.

</td>
</tr>
</table>
 




## -remarks



<b>ITextStoreACPSink::OnSelectionChange</b> is never called when the selection is modified by one of the <a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a> interface methods, such as <a href="https://msdn.microsoft.com/e9151b63-2ca7-4995-a36b-b919ab2d491a">ITextStoreACP::SetSelection</a> or <a href="https://msdn.microsoft.com/b57ad8da-6f79-4d27-96e0-608cbcaae826">ITextStoreACP::InsertTextAtSelection</a>.

When calling this method, the application must be able to grant a <a href="https://msdn.microsoft.com/3c623c44-b0d3-4b03-8de9-25f1062b5726">document lock</a>.




## -see-also




<a href="https://msdn.microsoft.com/3c623c44-b0d3-4b03-8de9-25f1062b5726">Document Locks</a>



<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP
      </a>



<a href="https://msdn.microsoft.com/b57ad8da-6f79-4d27-96e0-608cbcaae826">
        ITextStoreACP::InsertTextAtSelection
      </a>



<a href="https://msdn.microsoft.com/e9151b63-2ca7-4995-a36b-b919ab2d491a">
        ITextStoreACP::SetSelection
      </a>



<a href="https://msdn.microsoft.com/d7e5a04f-7159-436e-a522-4cb63063aeef">ITextStoreACPSink</a>
 

 


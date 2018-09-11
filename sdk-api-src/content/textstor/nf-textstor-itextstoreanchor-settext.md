---
UID: NF:textstor.ITextStoreAnchor.SetText
title: ITextStoreAnchor::SetText
author: windows-sdk-content
description: The ITextStoreAnchor::SetText method sets the text selection between two supplied anchor locations.
old-location: tsf\itextstoreanchor_settext.htm
tech.root: TSF
ms.assetid: 03beac03-cd09-4e03-b700-d96741e4932b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],SetText method, ITextStoreAnchor.SetText, ITextStoreAnchor::SetText, SetText, SetText method [Text Services Framework], SetText method [Text Services Framework],ITextStoreAnchor interface, textstor/ITextStoreAnchor::SetText, tsf.itextstoreanchor_settext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreAnchor.SetText
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreAnchor::SetText


## -description


The <b>ITextStoreAnchor::SetText</b> method sets the text selection between two supplied anchor locations.


## -parameters




### -param dwFlags [in]

If set to the value of TS_ST_CORRECTION, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier. The client defines the type of markup information to be retained.


### -param paStart [in]

Pointer to the anchor at the start of the range of text to replace.


### -param paEnd [in]

Pointer to the anchor at the end of the range of text to replace. Must always follow or be at the same position as <i>paStart</i>.


### -param pchText [in]

Pointer to the replacement text. The text string does not have to be <b>NULL</b> terminated, because the text character count is specified in the <i>cch</i> parameter.


### -param cch [in]

Specifies the number of characters in the replacement text.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method could not instantiate one of the anchors <i>paStart</i> or <i>paEnd</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
The location of <i>paStart</i> or <i>paEnd</i> is outside of the document text.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read/write lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
The document is read-only. Content cannot be modified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_REGION</b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to modify text across a region boundary.

</td>
</tr>
</table>
 




## -remarks



Applications should start a composition by first using <a href="https://msdn.microsoft.com/f5cb512a-d9f5-451f-b6cb-2020ba32e855">ITextStoreAnchor::InsertTextAtSelection</a>. <b>ITextStoreAnchor::SetText</b> should be used only within an existing composition. If there is no active composition at the time <b>SetText</b> is called, the TSF manager creates a composition that lasts just long enough to wrap the call to <b>SetText</b>.

Callers must hold a write lock obtained through <a href="https://msdn.microsoft.com/4cace5bd-d111-4a9a-af10-9ad454d4f2eb">ITextStoreAnchor::RequestLock</a>. Otherwise, <b>ITextStoreAnchor::SetText</b> will fail with TS_E_NOLOCK.

If <i>paStart</i> is at the same location as <i>paEnd</i>, then the operation is an insertion, and no existing text will be removed.

TS_CHAR_EMBEDDED cannot be passed into this method. For <a href="https://msdn.microsoft.com/44cb22b5-707b-4f21-b986-5258ed273543">embedded objects</a>, use <a href="https://msdn.microsoft.com/414842cc-7c3e-4f5c-93ac-3bd0eda5293e">ITextStoreAnchor::InsertEmbedded</a> instead.

This method will fail if the range of text replaced covers any region boundary. Instead, callers should make multiple calls to the method, one for each region.




## -see-also




<a href="https://msdn.microsoft.com/3d9da4f2-ceb9-4abc-8979-d3756d948a57">Compositions</a>



<a href="https://msdn.microsoft.com/44cb22b5-707b-4f21-b986-5258ed273543">Embedded Objects</a>



<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>



<a href="https://msdn.microsoft.com/414842cc-7c3e-4f5c-93ac-3bd0eda5293e">ITextStoreAnchor::InsertEmbedded
      </a>



<a href="https://msdn.microsoft.com/4cace5bd-d111-4a9a-af10-9ad454d4f2eb">ITextStoreAnchor::RequestLock
      </a>



<a href="https://msdn.microsoft.com/4bdf12bc-c15e-4bdb-8bc0-53172e9c943e">ITextStoreAnchorSink::OnTextChange
      </a>



<a href="https://msdn.microsoft.com/6e05ed74-fff3-4bc4-a21e-9af9492af23b">Miscellaneous Text Store Constants
      </a>
 

 


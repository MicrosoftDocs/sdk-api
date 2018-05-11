---
UID: NN:inputscope.ITfInputScope
title: ITfInputScope
author: windows-driver-content
description: The ITfInputScope interface is used by the text input processors to get the InputScope value that represents a document context associated with a window.
old-location: tsf\ITfInputScope.htm
old-project: TSF
ms.assetid: b2a045dd-dc2c-489d-bcb9-80710faef9c2
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITfInputScope, ITfInputScope interface [Text Services Framework], ITfInputScope interface [Text Services Framework],described, _tsf_itfinputscope_ref, inputscope/ITfInputScope, tsf.ITfInputScope
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: inputscope.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InputScope.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: InputScope
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfInputScope
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfInputScope interface


## -description


The <b>ITfInputScope</b> interface is used by the text input processors to get the <a href="https://msdn.microsoft.com/193a8a84-6824-4881-9399-832810957366">InputScope</a> value that represents a document context associated with a window. The input scope provides rules to help speech and handwriting recognition. For instance, if a text box on a form is used to enter an address, the input scope for that text box can be set to recognize and accept only those characters that are valid for an address.

The interface ID is IID_ITfInputScope.

The document context is used by the speech and handwriting recognition engine and is set by a text input processor by calling the <a href="https://msdn.microsoft.com/4098525c-8d29-419a-9484-9e70420416bc">SetInputScope</a> method. A TSF-aware application does not call <b>SetInputScope</b> directly, but rather implements either <a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a> or <a href="https://msdn.microsoft.com/630646df-dd47-4dbf-9787-f9d697ad8d7a">ITfContextOwner</a> to get a pointer to <b>ITfInputScope</b>.

To get the pointer to the <b>ITfInputScope</b> interface, the text input processor or TSF-aware application calls <a href="https://msdn.microsoft.com/5c04ff8e-5686-4802-b312-71dddaf0155e">ITfContext::GetAppProperty</a>, passing in <b>GUID_PROP_INPUTSCOPE</b> and a pointer to the <a href="https://msdn.microsoft.com/f4021a3d-6b86-469f-8943-770e7ef0cf99">ITFReadOnlyProperty</a> interface, as in the following example.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
extern const GUID GUID_PROP_INPUTSCOPE;
// 
// The TIP can call this to get the input scope of the document mgr. 
// 
HRESULT GetInputScope(ITfContext *pic, ITfRange *pRange, TfEditCookie ec, ITfInutScope **ppiscope){
    ITFReadOnlyProperty *prop;
    HRESULT hr;
    If (SUCCEEDED(hr = pic-&gt;GetAppProperty(GUID_PROP_INPUTSCOPE, &amp;prop))
    {   VARIANT var;
        If (SUCCEEDED(hr = prop-&gt;GetValue(ec, pRange, &amp;var)))
        {  hr = var.punkVal-&gt;QueryInterface(IID_ITfInputScope, (void **)ppiscope);
        }
        prop-&gt;Release();
    }
    return hr
}
</pre>
</td>
</tr>
</table></span></div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfInputScope</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfInputScope</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfInputScope</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5d54d2a-13b4-42f7-9224-4e80f0148a86">GetInputScopes</a>
</td>
<td align="left" width="63%">
Gets the input scopes that are associated with this context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a97dab0-2e3d-4921-80a6-0f2c79fbf4aa">GetPhrase</a>
</td>
<td align="left" width="63%">
Gets the phrase list set to this context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa24c473-efc7-408f-86e8-905161de10f0">GetRegularExpression</a>
</td>
<td align="left" width="63%">
Gets the regular expression string to be rssecognized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6514d925-b60e-4071-abb2-4c26a122089a">GetSRGS</a>
</td>
<td align="left" width="63%">
Gets the Speech Recognition Grammar Specification (SRGS) string to be recognized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e7a2780-6080-4f9a-b036-bc8f6258bcb5">GetXML</a>
</td>
<td align="left" width="63%">
Gets the custom XML string to be recognized.

</td>
</tr>
</table> 


## -remarks



To use this interface with window-less controls, an application has two options.

<ol>
<li><b>Make the application TSF-aware:  </b>A TSF-aware application must implement either <a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a> or <a href="https://msdn.microsoft.com/630646df-dd47-4dbf-9787-f9d697ad8d7a">ITfContextOwner</a> to get a pointer to <b>ITfInputScope</b>.</li>
<li>
<a href="https://msdn.microsoft.com/28c0be9b-f42c-4ab1-a3af-9c591a5192dd">SetInputScopes</a>  This is not recommended, but if the application is not TSF-aware, there is no other way to maintain the association between the input scope and the application. In this case, the application must call SetInputScopes whenever focus changes among window-less controls.</li>
</ol>



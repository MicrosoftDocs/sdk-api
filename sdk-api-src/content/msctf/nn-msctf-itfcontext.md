---
UID: NN:msctf.ITfContext
title: ITfContext
author: windows-sdk-content
description: The ITfContext interface is implemented by the TSF manager and used by applications and text services to access an edit context.
old-location: tsf\itfcontext.htm
old-project: TSF
ms.assetid: ca98c7bb-7348-405d-976a-18012b0886c6
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfContext, ITfContext interface [Text Services Framework], ITfContext interface [Text Services Framework],described, _tsf_itfcontext_ref, msctf/ITfContext, tsf.itfcontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ITfContext
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfContext interface


## -description


The <b>ITfContext</b> interface is implemented by the TSF manager and used by applications and text services to access an edit context.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfContext</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3b52170-af1b-407b-9160-1265ae3c9afc">CreateRangeBackup</a>
</td>
<td align="left" width="63%">
Creates a backup of a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b57c9fdc-320b-4d97-8af4-c75756326437">EnumProperties</a>
</td>
<td align="left" width="63%">
Obtains a document property enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/baf09cb2-fa0e-470c-ad68-3e0187673aab">EnumViews</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41f7eb74-bca2-4d53-8a70-0b872616fd1b">GetActiveView</a>
</td>
<td align="left" width="63%">
Obtains the active view for the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c04ff8e-5686-4802-b312-71dddaf0155e">GetAppProperty</a>
</td>
<td align="left" width="63%">
Obtains an application property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21fa683d-c386-4aa2-8bc5-d5170443c5cd">GetDocumentMgr</a>
</td>
<td align="left" width="63%">
Obtains the document manager that contains the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4fdae76d-ad02-43a4-8a39-418cae847ae8">GetEnd</a>
</td>
<td align="left" width="63%">
Obtains a range of text positioned at the end of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5d76443-f767-47fb-be3a-8cbac224d299">GetProperty</a>
</td>
<td align="left" width="63%">
Obtains a text property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08b67fd5-aebe-49f7-af78-6f49c8f47f64">GetSelection</a>
</td>
<td align="left" width="63%">
Obtains the selection within the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3108da05-c38f-4f0c-a16a-1f7e5f05d475">GetStart</a>
</td>
<td align="left" width="63%">
Obtains a range of text positioned at the beginning of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406321">GetStatus</a>
</td>
<td align="left" width="63%">
Obtains the document status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88a8a2c1-bd5f-47d2-8612-c7e0cabfe254">InWriteSession</a>
</td>
<td align="left" width="63%">
Determines if a client has a read/write lock on the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c7b150c-0ca0-4aa5-8828-0c548dbfb215">RequestEditSession</a>
</td>
<td align="left" width="63%">
Obtains access to the document text and properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1cf50b5e-6ec2-4649-9acc-743a2e3d8096">SetSelection</a>
</td>
<td align="left" width="63%">
Sets the selection within the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e283a45d-b585-4a26-89db-7ed706f0f593">TrackProperties</a>
</td>
<td align="left" width="63%">
Obtains a special property that can enumerate multiple properties over multiple ranges.

</td>
</tr>
</table> 


## -remarks



An edit context object is created by calling <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a>. Often, a text service uses the currently active edit context. The currently active edit context is the edit context at the top of the stack of the active document manager.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT         hr;
ITfDocumentMgr  *pFocusDoc;

hr = pThreadMgr-&gt;GetFocus(&amp;pFocusDoc);
if(SUCCEEDED(hr))
{
    ITfContext *pContext;

    hr = pFocusDoc-&gt;GetTop(&amp;pContext);
    if(SUCCEEDED(hr))
    {
        //Use the context. 
        
        pContext-&gt;Release();
    }

    pFocusDoc-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/cf8bbe66-d2ad-49b3-9e7c-246e4ca50149">Edit Contexts</a>



<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 


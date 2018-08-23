---
UID: NF:strmif.IPersistMediaPropertyBag.Load
title: IPersistMediaPropertyBag::Load
author: windows-sdk-content
description: The Load method loads properties from the media property bag into the filter.
old-location: dshow\ipersistmediapropertybag_load.htm
old-project: DirectShow
ms.assetid: 02ee3911-0b85-404d-81c9-7d0e6b3ccd5d
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IPersistMediaPropertyBag interface [DirectShow],Load method, IPersistMediaPropertyBag.Load, IPersistMediaPropertyBag::Load, IPersistMediaPropertyBagLoad, Load, Load method [DirectShow], Load method [DirectShow],IPersistMediaPropertyBag interface, dshow.ipersistmediapropertybag_load, strmif/IPersistMediaPropertyBag::Load
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IPersistMediaPropertyBag.Load
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IPersistMediaPropertyBag::Load


## -description



The <code>Load</code> method loads properties from the media property bag into the filter.




## -parameters




### -param pPropBag [in]

Pointer to the <a href="https://msdn.microsoft.com/6f134160-b0aa-44fd-b1b9-938f11349eac">IMediaPropertyBag</a> interface of a media property bag created by the caller.


### -param pErrorLog [in]

Reserved. Set the value to <b>NULL</b>.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Access denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
Filter graph is not in a stopped state.

</td>
</tr>
</table>
 




## -remarks



Call this method on the <a href="https://msdn.microsoft.com/31d30c91-fc6a-45ec-a2e0-34e6a1e902a4">AVI Mux</a> filter to write the properties into the AVI stream. Call the method when the filter is stopped, before you run the filter graph to author the file. When the graph runs, the filter writes the INFO chunks into the AVI header.

The following code example adds an IART (author name) INFO chunk to a file:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IPersistMediaPropertyBag *pPersist = NULL;
IMediaPropertyBag *pBag = NULL;
VARIANT val;

// Query the AVI Mux filter for IPersistMediaPropertyBag (not shown).

CoCreateInstance(CLSID_MediaPropertyBag, NULL, CLSCTX_INPROC,
        IID_IMediaPropertyBag, (LPVOID *)&amp;pBag);

val.vt = VT_BSTR;
val.bstrVal = SysAllocString(OLESTR("Author Name"));
pBag-&gt;Write(OLESTR("INFO/IART"), &amp;val);
pPersist-&gt;Load(pBag, NULL);
VariantClear(&amp;val);
</pre>
</td>
</tr>
</table></span></div>
The <a href="https://msdn.microsoft.com/df3c7d11-7ecc-499a-af36-b74437e21999">AVI Splitter</a> filter and the <a href="https://msdn.microsoft.com/53a9538d-7a79-40bb-9468-d710eb238925">WAVE Parser</a> do not support this method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/33e4b76b-841a-4dc5-b117-e08a6f4dcbe7">IPersistMediaPropertyBag Interface</a>
 

 


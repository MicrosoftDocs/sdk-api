---
UID: NF:sbe.IStreamBufferInitialize.SetHKEY
title: IStreamBufferInitialize::SetHKEY
author: windows-driver-content
description: The SetHKEY method sets the registry key where the stream buffer object stores its configuration information.
old-location: mstv\istreambufferinitialize_sethkey.htm
old-project: mstv
ms.assetid: f8d85180-2575-4525-9b8a-bec354e2cd4c
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IStreamBufferInitialize interface [Microsoft TV Technologies],SetHKEY method, IStreamBufferInitialize.SetHKEY, IStreamBufferInitialize::SetHKEY, IStreamBufferInitializeSetHKEY, SetHKEY, SetHKEY method [Microsoft TV Technologies], SetHKEY method [Microsoft TV Technologies],IStreamBufferInitialize interface, mstv.istreambufferinitialize_sethkey, sbe/IStreamBufferInitialize::SetHKEY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Sbe.h
api_name:
-	IStreamBufferInitialize.SetHKEY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IStreamBufferInitialize::SetHKEY


## -description


The <b>SetHKEY</b> method sets the registry key where the stream buffer object stores its configuration information.


## -parameters




### -param hkeyRoot [in]

Handle to the registry key.


## -returns



Returns an <b>HRESULT</b>. Possible values include those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
<b>SetHKEY</b> was called on a filter after it initialized internally.

</td>
</tr>
</table>
 




## -remarks



This method enables an application to specify a registry key where the stream buffer objects will save configuration information, including the location of the backing files, the number of backing files, and their size.

You must call this method before the object is initialized, either explicitly or implicitly. For the Stream Buffer Sink filter, call the method before the profile is locked. For the Stream Buffer Source filter, call the method before setting the source file name.

To use this method, do the following:

<ol>
<li>Create a new registry key or open an existing key.</li>
<li>Create an instance of the <b>StreamBufferConfig</b> object.</li>
<li>Query the <b>StreamBufferConfig</b> object for the <b>IStreamBufferInitialize</b> interface.</li>
<li>Call <b>SetHKey</b> on the <b>StreamBufferConfig</b> object, with a handle to the registry key.</li>
<li>Optionally, call <b>IStreamBufferConfigure</b> methods to modify the configuration information that will be stored in the registry key.</li>
<li>Call <b>SetHKey</b> on the Stream Buffer Source filter and the Stream Buffer Sink filter, using the same registry key.</li>
</ol>
The application is responsible for ensuring that the user has read/write permissions for the registry key.

The caller may release the registry key handle after calling this method.


#### Examples

The following code shows how to configure the backing file directory. Error checking is omitted for brevity.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Create the StreamBufferConfig object.
CComPtr&lt;IStreamBufferConfigure&gt; pConfig;
hr = pConfig.CoCreateInstance(CLSID_StreamBufferConfig);

// Create a new registry key to hold our settings.
HKEY hkey = 0;
long lRes = RegCreateKey(HKEY_LOCAL_MACHINE,
    TEXT("SOFTWARE\\MyStreamBufferKey"), &amp;hkey);

// Set the registry key.
CComPtr&lt;IStreamBufferInitialize&gt; pInit;
hr = pConfig.QueryInterface(&amp;pInit);
hr = pInit-&gt;SetHKEY(hkey);
pInit.Release();

// Set the backing file directory.
hr = pConfig-&gt;SetDirectory(L"C:\\MyDirectory");

// Create the Stream Buffer Sink filter and set the registry key.
CComPtr&lt;IStreamBufferSink&gt; pSink;
hr = pSink.CoCreateInstance(CLSID_StreamBufferSink);
hr = pSink.QueryInterface(&amp;pInit);
hr = pInit-&gt;SetHKEY(hkey);
pInit.Release();

// Create the Stream Buffer Source filter and set the registry key.
CComPtr&lt;IStreamBufferSource&gt; pSource;
hr = pSource.CoCreateInstance(CLSID_StreamBufferSource);
hr = pSource.QueryInterface(&amp;pInit);
hr = pInit-&gt;SetHKEY(hkey);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/357b2979-78de-4a99-bf52-4117af7dfaad">IStreamBufferInitialize Interface</a>
 

 


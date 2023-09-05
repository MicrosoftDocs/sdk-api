---
UID: NF:sbe.IStreamBufferInitialize.SetHKEY
title: IStreamBufferInitialize::SetHKEY (sbe.h)
description: The SetHKEY method sets the registry key where the stream buffer object stores its configuration information.
helpviewer_keywords: ["IStreamBufferInitialize interface [Microsoft TV Technologies]","SetHKEY method","IStreamBufferInitialize.SetHKEY","IStreamBufferInitialize::SetHKEY","IStreamBufferInitializeSetHKEY","SetHKEY","SetHKEY method [Microsoft TV Technologies]","SetHKEY method [Microsoft TV Technologies]","IStreamBufferInitialize interface","mstv.istreambufferinitialize_sethkey","sbe/IStreamBufferInitialize::SetHKEY"]
old-location: mstv\istreambufferinitialize_sethkey.htm
tech.root: mstv
ms.assetid: f8d85180-2575-4525-9b8a-bec354e2cd4c
ms.date: 12/05/2018
ms.keywords: IStreamBufferInitialize interface [Microsoft TV Technologies],SetHKEY method, IStreamBufferInitialize.SetHKEY, IStreamBufferInitialize::SetHKEY, IStreamBufferInitializeSetHKEY, SetHKEY, SetHKEY method [Microsoft TV Technologies], SetHKEY method [Microsoft TV Technologies],IStreamBufferInitialize interface, mstv.istreambufferinitialize_sethkey, sbe/IStreamBufferInitialize::SetHKEY
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStreamBufferInitialize::SetHKEY
 - sbe/IStreamBufferInitialize::SetHKEY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferInitialize.SetHKEY
---

# IStreamBufferInitialize::SetHKEY


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

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


```cpp

// Create the StreamBufferConfig object.
CComPtr<IStreamBufferConfigure> pConfig;
hr = pConfig.CoCreateInstance(CLSID_StreamBufferConfig);

// Create a new registry key to hold our settings.
HKEY hkey = 0;
long lRes = RegCreateKey(HKEY_LOCAL_MACHINE,
    TEXT("SOFTWARE\\MyStreamBufferKey"), &hkey);

// Set the registry key.
CComPtr<IStreamBufferInitialize> pInit;
hr = pConfig.QueryInterface(&pInit);
hr = pInit->SetHKEY(hkey);
pInit.Release();

// Set the backing file directory.
hr = pConfig->SetDirectory(L"C:\\MyDirectory");

// Create the Stream Buffer Sink filter and set the registry key.
CComPtr<IStreamBufferSink> pSink;
hr = pSink.CoCreateInstance(CLSID_StreamBufferSink);
hr = pSink.QueryInterface(&pInit);
hr = pInit->SetHKEY(hkey);
pInit.Release();

// Create the Stream Buffer Source filter and set the registry key.
CComPtr<IStreamBufferSource> pSource;
hr = pSource.CoCreateInstance(CLSID_StreamBufferSource);
hr = pSource.QueryInterface(&pInit);
hr = pInit->SetHKEY(hkey);

```

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferinitialize">IStreamBufferInitialize Interface</a>
---
UID: NF:mfreadwrite.IMFReadWriteClassFactory.CreateInstanceFromObject
title: IMFReadWriteClassFactory::CreateInstanceFromObject
author: windows-sdk-content
description: Creates an instance of the sink writer or source reader, given an IUnknown pointer.
old-location: mf\imfreadwriteclassfactory_createinstancefromobject.htm
old-project: medfound
ms.assetid: 5da582c2-37f9-47ee-b8ea-d21f1323f1df
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: CLSID_MFSinkWriter, CLSID_MFSourceReader, CreateInstanceFromObject, CreateInstanceFromObject method [Media Foundation], CreateInstanceFromObject method [Media Foundation],IMFReadWriteClassFactory interface, IMFByteStream, IMFMediaSink, IMFMediaSource, IMFReadWriteClassFactory interface [Media Foundation],CreateInstanceFromObject method, IMFReadWriteClassFactory.CreateInstanceFromObject, IMFReadWriteClassFactory::CreateInstanceFromObject, mf.imfreadwriteclassfactory_createinstancefromobject, mfreadwrite/IMFReadWriteClassFactory::CreateInstanceFromObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfreadwrite.h
api_name:
-	IMFReadWriteClassFactory.CreateInstanceFromObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFReadWriteClassFactory::CreateInstanceFromObject


## -description


Creates an instance of the sink writer or source reader, given an <b>IUnknown</b> pointer. 


## -parameters




### -param clsid [in]

The CLSID of the object to create.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLSID_MFSinkWriter"></a><a id="clsid_mfsinkwriter"></a><a id="CLSID_MFSINKWRITER"></a><dl>
<dt><b><b>CLSID_MFSinkWriter</b></b></dt>
</dl>
</td>
<td width="60%">
Create the sink writer. The <i>ppvObject</i> parameter receives an <a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a> interface pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="CLSID_MFSourceReader"></a><a id="clsid_mfsourcereader"></a><a id="CLSID_MFSOURCEREADER"></a><dl>
<dt><b><b>CLSID_MFSourceReader</b></b></dt>
</dl>
</td>
<td width="60%">
Create the source reader. The <i>ppvObject</i> parameter receives an <a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a> interface pointer.

</td>
</tr>
</table>
 


### -param punkObject [in]

A pointer to the <b>IUnknown</b> interface of an object that is used to initialize the source reader or sink writer. The method queries this pointer for one of the following interfaces.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMFByteStream"></a><a id="imfbytestream"></a><a id="IMFBYTESTREAM"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a></b></dt>
</dl>
</td>
<td width="60%">
Pointer to a byte stream. 

If <i>clsid</i> is <b>CLSID_MFSinkWriter</b>, the sink writer writes data to this byte stream.

If <i>clsid</i> is <b>CLSID_MFSourceReader</b>, this byte stream provides the source data for the source reader.

</td>
</tr>
<tr>
<td width="40%"><a id="IMFMediaSink"></a><a id="imfmediasink"></a><a id="IMFMEDIASINK"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a></b></dt>
</dl>
</td>
<td width="60%">
Pointer to a media sink. Applies only when <i>clsid</i> is <b>CLSID_MFSinkWriter</b>. 

</td>
</tr>
<tr>
<td width="40%"><a id="IMFMediaSource"></a><a id="imfmediasource"></a><a id="IMFMEDIASOURCE"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a></b></dt>
</dl>
</td>
<td width="60%">
Pointer to a media source. Applies only when <i>clsid</i> is <b>CLSID_MFSourceReader</b>.

</td>
</tr>
</table>
 


### -param pAttributes [in]

A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. You can use this parameter to configure the sink writer or source reader. For more information, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/f27b9beb-f35f-400e-a337-50d9de21e91e">Sink Writer Attributes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/312a588a-848b-4563-893a-fac49a4ca465">Source Reader Attributes</a>
</li>
</ul>
This parameter can be <b>NULL</b>.


### -param riid [in]

The IID of the requested interface.


### -param ppvObject [out]

Receives a pointer to the requested interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/83ef0f0a-ae60-474d-a9e7-7c83a73f6255">IMFReadWriteClassFactory</a>
 

 


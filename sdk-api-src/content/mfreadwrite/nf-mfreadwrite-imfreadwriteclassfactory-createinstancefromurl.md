---
UID: NF:mfreadwrite.IMFReadWriteClassFactory.CreateInstanceFromURL
title: IMFReadWriteClassFactory::CreateInstanceFromURL
author: windows-driver-content
description: Creates an instance of the sink writer or source reader, given a URL.
old-location: mf\imfreadwriteclassfactory_createinstancefromurl.htm
old-project: medfound
ms.assetid: 2769faa2-e381-4908-95f8-122ae4cd7ec5
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CLSID_MFSinkWriter, CLSID_MFSourceReader, CreateInstanceFromURL, CreateInstanceFromURL method [Media Foundation], CreateInstanceFromURL method [Media Foundation],IMFReadWriteClassFactory interface, IMFReadWriteClassFactory interface [Media Foundation],CreateInstanceFromURL method, IMFReadWriteClassFactory.CreateInstanceFromURL, IMFReadWriteClassFactory::CreateInstanceFromURL, mf.imfreadwriteclassfactory_createinstancefromurl, mfreadwrite/IMFReadWriteClassFactory::CreateInstanceFromURL
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfreadwrite.h
api_name:
-	IMFReadWriteClassFactory.CreateInstanceFromURL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFReadWriteClassFactory::CreateInstanceFromURL


## -description


Creates an instance of the sink writer or source reader, given a URL.


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
 


### -param pwszURL [in]

A null-terminated string that contains a URL. If <i>clsid</i> is CLSID_<b>MFSinkWriter</b>, the URL specifies the name of the output file. The sink writer creates a new file with this name. If <i>clsid</i> is <b>CLSID_MFSourceReader</b>, the URL specifies the input file for the source reader.


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
 

 


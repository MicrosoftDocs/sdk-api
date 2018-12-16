---
UID: NF:wmcontainer.MFCreateASFIndexerByteStream
title: MFCreateASFIndexerByteStream function
author: windows-sdk-content
description: Creates a byte stream to access the index in an ASF stream.
old-location: mf\mfcreateasfindexerbytestream.htm
tech.root: medfound
ms.assetid: edcce9d4-9296-4b39-8e58-58ae602c250f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MFCreateASFIndexerByteStream, MFCreateASFIndexerByteStream function [Media Foundation], edcce9d4-9296-4b39-8e58-58ae602c250f, mf.mfcreateasfindexerbytestream, wmcontainer/MFCreateASFIndexerByteStream
ms.topic: function
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateASFIndexerByteStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateASFIndexerByteStream function


## -description



Creates a byte stream to access the index in an ASF stream.




## -parameters




### -param pIContentByteStream [in]

Pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of a byte stream that contains the ASF stream.


### -param cbIndexStartOffset [in]

Byte offset of the index within the ASF stream. To get this value, call <a href="https://msdn.microsoft.com/7ef0e36c-1be5-44ac-8f6a-e29805c99e78">IMFASFIndexer::GetIndexPosition</a>.


### -param pIIndexByteStream [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface. Use this interface to read from the index or write to the index. The caller must release the interface.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table:

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
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The offset specified in <i>cbIndexStartOffset</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 


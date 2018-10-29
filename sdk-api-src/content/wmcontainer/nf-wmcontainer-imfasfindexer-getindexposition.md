---
UID: NF:wmcontainer.IMFASFIndexer.GetIndexPosition
title: IMFASFIndexer::GetIndexPosition
author: windows-sdk-content
description: Retrieves the offset of the index object from the start of the content.
old-location: mf\imfasfindexer_getindexposition.htm
tech.root: medfound
ms.assetid: 7ef0e36c-1be5-44ac-8f6a-e29805c99e78
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 7ef0e36c-1be5-44ac-8f6a-e29805c99e78, GetIndexPosition, GetIndexPosition method [Media Foundation], GetIndexPosition method [Media Foundation],IMFASFIndexer interface, IMFASFIndexer interface [Media Foundation],GetIndexPosition method, IMFASFIndexer.GetIndexPosition, IMFASFIndexer::GetIndexPosition, mf.imfasfindexer_getindexposition, wmcontainer/IMFASFIndexer::GetIndexPosition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFIndexer.GetIndexPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFIndexer::GetIndexPosition


## -description



Retrieves the offset of the index object from the start of the content.




## -parameters




### -param pIContentInfo [in]

Pointer to the <a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a> interface of the ContentInfo object that describes the content.


### -param pcbIndexOffset [out]

Receives the offset of the index relative to the beginning of the content described by the ContentInfo object. This is the position relative to the beginning of the ASF file.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pIContentInfo</i> is <b>NULL</b> or <i>pcbIndexOffset</i> is <b>NULL</b>

</td>
</tr>
</table>
 




## -remarks



The index continues from the offset retrieved by this method to the end of the file.

You must call <a href="https://msdn.microsoft.com/c02931d3-7b43-43a9-9e4e-00945ba3c8d8">IMFASFIndexer::Initialize</a> to set up the indexer before calling this method.

If the index is retrieved by using more than one call to <a href="https://msdn.microsoft.com/aca721e8-e610-4022-a3da-8ff5a5943e3e">IMFASFIndexer::GetCompletedIndex</a>, the position of individual index portions is equal to the index offset plus the offset of the portion within the index.




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a>
 

 


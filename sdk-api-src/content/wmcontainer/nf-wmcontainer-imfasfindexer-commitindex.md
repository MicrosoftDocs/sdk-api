---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMFASFIndexer::CommitIndex


## -description



Adds information about a new index to the ContentInfo object associated with ASF content. You must call this method before copying the index to the content so that the index will be readable by the indexer later.




## -parameters




### -param pIContentInfo [in]

Pointer to the <a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a> interface of the ContentInfo object that describes the content.


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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The caller made an invalid request. For more information, see Remarks.

</td>
</tr>
</table>
 




## -remarks



For the index to function properly, you must call this method after all ASF packets in the file have been passed to the indexer by using the <a href="https://msdn.microsoft.com/febc5335-a8e8-4ae9-afb2-17f09b750477">IMFASFIndexer::GenerateIndexEntries</a> method. After you call this method, you must retrieve the indexes by calling <a href="https://msdn.microsoft.com/aca721e8-e610-4022-a3da-8ff5a5943e3e">GetCompletedIndex</a> and write them to the appropriate location in the file. Finally, you must generate a new ASF header by calling the <a href="https://msdn.microsoft.com/972f5ae7-ad00-4c3b-8ec4-2cef4ce03c4e">IMFASFContentInfo::GenerateHeader</a> method of the ASF ContentInfo object.

 An application must use the <b>CommitIndex</b> method only when writing a new index otherwise <b>CommitIndex</b> may return MF_E_INVALIDREQUEST as a result. For example, MF_E_INVALIDREQUEST is returned if the application has flags other than MFASF_INDEXER_WRITE_NEW_INDEX  set on the indexer object. <b>CommitIndex</b> can also return MFASF_INDEXER_WRITE_NEW_INDEX if the index entries have already been committed through an earlier <b>CommitIndex</b> call.

You cannot use this method in an index reading scenario.  You can only use this method when writing indexes.




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a>



<a href="https://msdn.microsoft.com/df141f8e-10b4-4ac4-8a83-c25764b8f0c6">MFCreateASFIndexer</a>
 

 


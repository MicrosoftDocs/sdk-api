---
UID: NF:wmcontainer.IMFASFIndexer.GetFlags
title: IMFASFIndexer::GetFlags (wmcontainer.h)
author: windows-sdk-content
description: Retrieves the flags that indicate the selected indexer options.
old-location: mf\imfasfindexer_getflags.htm
tech.root: medfound
ms.assetid: 97809620-57ad-48f1-94ba-a2e121cdfee6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 97809620-57ad-48f1-94ba-a2e121cdfee6, GetFlags, GetFlags method [Media Foundation], GetFlags method [Media Foundation],IMFASFIndexer interface, IMFASFIndexer interface [Media Foundation],GetFlags method, IMFASFIndexer.GetFlags, IMFASFIndexer::GetFlags, mf.imfasfindexer_getflags, wmcontainer/IMFASFIndexer::GetFlags
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
 - IMFASFIndexer.GetFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFIndexer::GetFlags


## -description



Retrieves the flags that indicate the selected indexer options.




## -parameters




### -param pdwFlags [out]

Receives a bitwise OR of zero or more flags from the <a href="https://msdn.microsoft.com/e5794835-218d-4759-bf3e-a573b24424c3">MFASF_INDEXER_FLAGS</a> enumeration.


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
<i>pdwFlags</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



You must call this method before initializing the indexer object with <a href="https://msdn.microsoft.com/c02931d3-7b43-43a9-9e4e-00945ba3c8d8">IMFASFIndexer::Initialize</a>.




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a>
 

 


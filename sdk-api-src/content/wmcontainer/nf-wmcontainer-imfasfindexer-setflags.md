---
UID: NF:wmcontainer.IMFASFIndexer.SetFlags
title: IMFASFIndexer::SetFlags
author: windows-sdk-content
description: Sets indexer options.
old-location: mf\imfasfindexer_setflags.htm
old-project: medfound
ms.assetid: 7df6aba2-d63f-4a1a-b6e8-6894f92993b1
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 7df6aba2-d63f-4a1a-b6e8-6894f92993b1, IMFASFIndexer interface [Media Foundation],SetFlags method, IMFASFIndexer.SetFlags, IMFASFIndexer::SetFlags, SetFlags, SetFlags method [Media Foundation], SetFlags method [Media Foundation],IMFASFIndexer interface, mf.imfasfindexer_setflags, wmcontainer/IMFASFIndexer::SetFlags
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFASFIndexer.SetFlags
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFIndexer::SetFlags


## -description



Sets indexer options.




## -parameters




### -param dwFlags [in]

Bitwise OR of zero or more flags from the <a href="https://msdn.microsoft.com/e5794835-218d-4759-bf3e-a573b24424c3">MFASF_INDEXER_FLAGS</a> enumeration specifying the indexer options to use.


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
The indexer object was  initialized before setting flags for it.  For more information, see Remarks.

</td>
</tr>
</table>
 




## -remarks



<b>IMFASFIndexer::SetFlags</b> must be called before <a href="https://msdn.microsoft.com/c02931d3-7b43-43a9-9e4e-00945ba3c8d8">IMFASFIndexer::Initialize</a>. Attempting to call <b>SetFlags</b> after <b>Initialize</b> will return MF_E_INVALIDREQUEST as a result.




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a>
 

 


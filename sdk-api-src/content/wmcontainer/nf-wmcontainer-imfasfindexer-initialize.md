---
UID: NF:wmcontainer.IMFASFIndexer.Initialize
title: IMFASFIndexer::Initialize
author: windows-driver-content
description: Initializes the indexer object.
old-location: mf\imfasfindexer_initialize.htm
old-project: medfound
ms.assetid: c02931d3-7b43-43a9-9e4e-00945ba3c8d8
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IMFASFIndexer interface [Media Foundation],Initialize method, IMFASFIndexer.Initialize, IMFASFIndexer::Initialize, Initialize, Initialize method [Media Foundation], Initialize method [Media Foundation],IMFASFIndexer interface, c02931d3-7b43-43a9-9e4e-00945ba3c8d8, mf.imfasfindexer_initialize, wmcontainer/IMFASFIndexer::Initialize
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
-	IMFASFIndexer.Initialize
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFIndexer::Initialize


## -description



Initializes the indexer object. This method reads information in a ContentInfo object about the configuration of the content and the properties of the existing index, if present. Use this method before using the indexer for either writing or reading an index. You must make this call before using any of the other methods of the <a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a> interface.




## -parameters




### -param pIContentInfo [in]

Pointer to the <a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a> interface of the ContentInfo object describing the content with which to use the indexer.


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
<dt><b>MF_E_ASF_INVALIDDATA</b></dt>
</dl>
</td>
<td width="60%">
Invalid ASF data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

</td>
</tr>
</table>
 




## -remarks



The indexer needs to examine the data in the ContentInfo object to properly write or read the index for the content. The indexer will not make changes to the content information and will not hold any references to the <a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a> interface.

In the ASF header, the maximum data-packet size must equal the minimum data-packet size. Otherwise, the method returns <b>MF_E_UNEXPECTED</b>.




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a>
 

 


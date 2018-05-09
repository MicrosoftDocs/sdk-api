---
UID: NF:textstor.ITextStoreAnchor.GetStatus
title: ITextStoreAnchor::GetStatus
author: windows-driver-content
description: The ITextStoreAnchor::GetStatus method obtains the document status. The document status is returned through the TS_STATUS structure.
old-location: tsf\itextstoreanchor_getstatus.htm
old-project: TSF
ms.assetid: 61192268-5a5f-4caa-bdb8-799ee4aea24e
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: GetStatus, GetStatus method [Text Services Framework], GetStatus method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],GetStatus method, ITextStoreAnchor.GetStatus, ITextStoreAnchor::GetStatus, textstor/ITextStoreAnchor::GetStatus, tsf.itextstoreanchor_getstatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITextStoreAnchor.GetStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreAnchor::GetStatus


## -description


The <b>ITextStoreAnchor::GetStatus</b> method obtains the document status. The document status is returned through the <a href="https://msdn.microsoft.com/d27d81f2-8599-4b65-866b-4e8fd2f589f5">TS_STATUS</a> structure.


## -parameters




### -param pdcs [out]

Receives the <a href="https://msdn.microsoft.com/d27d81f2-8599-4b65-866b-4e8fd2f589f5">TS_STATUS</a> structure that contains the document status. Cannot be <b>NULL</b>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The pointer to the TS_STATUS parameter is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">
        ITextStoreAnchor
      </a>



<a href="https://msdn.microsoft.com/28bdfa93-29c1-4a9f-b85e-20c39a1b429b">
        ITextStoreAnchorSink::OnStatusChange
      </a>



<a href="https://msdn.microsoft.com/ce30ec8a-48fe-4ec7-a7e1-2a0cf084097d">ITfContextOwner::GetStatus
      </a>



<a href="https://msdn.microsoft.com/d27d81f2-8599-4b65-866b-4e8fd2f589f5">
        TS_STATUS
      </a>
 

 


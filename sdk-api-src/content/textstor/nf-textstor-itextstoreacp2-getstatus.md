---
UID: NF:textstor.ITextStoreACP2.GetStatus
title: ITextStoreACP2::GetStatus
author: windows-sdk-content
description: Gets the document status. The document status is returned through the TS_STATUS structure.
old-location: tsf\itextstoreacp2_getstatus.htm
tech.root: TSF
ms.assetid: 6b767f85-0a92-467c-b358-3629582f0d43
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetStatus, GetStatus method [Text Services Framework], GetStatus method [Text Services Framework],ITextStoreACP2 interface, ITextStoreACP2 interface [Text Services Framework],GetStatus method, ITextStoreACP2.GetStatus, ITextStoreACP2::GetStatus, textstor/ITextStoreACP2::GetStatus, tsf.itextstoreacp2_getstatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITextStoreACP2.GetStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- textstor.h
: 
- ITextStoreACP2.GetStatus
: 
---

# ITextStoreACP2::GetStatus


## -description


Gets the document status. The document status is returned through the <a href="https://msdn.microsoft.com/d27d81f2-8599-4b65-866b-4e8fd2f589f5">TS_STATUS</a> structure.


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
The pointer to the <a href="https://msdn.microsoft.com/d27d81f2-8599-4b65-866b-4e8fd2f589f5">TS_STATUS</a> parameter is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP
      </a>



<a href="https://msdn.microsoft.com/c256f1c2-6b67-4417-8707-3490a2c5cb55">ITextStoreACP2</a>



<a href="https://msdn.microsoft.com/ce30ec8a-48fe-4ec7-a7e1-2a0cf084097d">ITfContextOwner::GetStatus
      </a>



<a href="https://msdn.microsoft.com/d27d81f2-8599-4b65-866b-4e8fd2f589f5">TS_STATUS</a>
 

 


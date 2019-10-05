---
UID: NF:textstor.ITextStoreACP.GetStatus
title: ITextStoreACP::GetStatus (textstor.h)
author: windows-sdk-content
description: The ITextStoreACP::GetStatus method obtains the document status. The document status is returned through the TS_STATUS structure.
old-location: tsf\itextstoreacp_getstatus.htm
tech.root: TSF
ms.assetid: 6ed040ac-8584-4f09-9af8-218b5cd33765
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Text Services Framework], GetStatus method [Text Services Framework],ITextStoreACP interface, ITextStoreACP interface [Text Services Framework],GetStatus method, ITextStoreACP.GetStatus, ITextStoreACP::GetStatus, _tsf_itextstoreacp_getstatus_ref, textstor/ITextStoreACP::GetStatus, tsf.itextstoreacp_getstatus
ms.topic: method
f1_keywords: 
 - "textstor/ITextStoreACP.GetStatus"
dev_langs:
 - c++
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITextStoreACP.GetStatus
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITextStoreACP::GetStatus


## -description


The <b>ITextStoreACP::GetStatus</b> method obtains the document status. The document status is returned through the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/ns-textstor-ts_status">TS_STATUS</a> structure.


## -parameters




### -param pdcs [out]

Receives the <b>TS_STATUS</b> structure that contains the document status. Cannot be <b>NULL</b>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextowner-getstatus">ITfContextOwner::GetStatus
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/ns-textstor-ts_status">TS_STATUS
      </a>
 

 


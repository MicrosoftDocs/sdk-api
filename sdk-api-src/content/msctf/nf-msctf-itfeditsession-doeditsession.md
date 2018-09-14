---
UID: NF:msctf.ITfEditSession.DoEditSession
title: ITfEditSession::DoEditSession
author: windows-sdk-content
description: ITfEditSession::DoEditSession method
old-location: tsf\itfeditsession_doeditsession.htm
tech.root: TSF
ms.assetid: f89b2676-9a69-492f-be8a-96e4436d594c
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: DoEditSession, DoEditSession method [Text Services Framework], DoEditSession method [Text Services Framework],ITfEditSession interface, ITfEditSession interface [Text Services Framework],DoEditSession method, ITfEditSession.DoEditSession, ITfEditSession::DoEditSession, _tsf_itfeditsession_doeditsession_ref, msctf/ITfEditSession::DoEditSession, tsf.itfeditsession_doeditsession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Tipskins.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tipskins.dll
api_name:
 - ITfEditSession.DoEditSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfEditSession::DoEditSession


## -description




## -parameters




### -param ec [in]

Contains a <a href="https://msdn.microsoft.com/1de17286-5d56-4302-a144-5fe6ca7d5557">TfEditCookie</a> value that uniquely identifies the edit session. This cookie is used to access the context with methods such as <a href="https://msdn.microsoft.com/b38a8de3-947f-469c-9f0d-f0482ea86884">ITfRange::GetText</a>.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6c7b150c-0ca0-4aa5-8828-0c548dbfb215">ITfContext::RequestEditSession
      </a>



<a href="https://msdn.microsoft.com/b9d4718a-42a6-4be5-9f57-1a392cd98469">ITfEditSession
      </a>



<a href="https://msdn.microsoft.com/b38a8de3-947f-469c-9f0d-f0482ea86884">ITfRange::GetText</a>



<a href="https://msdn.microsoft.com/1de17286-5d56-4302-a144-5fe6ca7d5557">TfEditCookie
      </a>
 

 


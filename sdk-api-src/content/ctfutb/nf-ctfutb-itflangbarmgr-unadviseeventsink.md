---
UID: NF:ctfutb.ITfLangBarMgr.UnadviseEventSink
title: ITfLangBarMgr::UnadviseEventSink (ctfutb.h)
author: windows-sdk-content
description: ITfLangBarMgr::UnadviseEventSink method
old-location: tsf\itflangbarmgr_unadviseeventsink.htm
tech.root: TSF
ms.assetid: 29dc5276-04fa-4219-a64d-10d775d73fdd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfLangBarMgr interface [Text Services Framework],UnadviseEventSink method, ITfLangBarMgr.UnadviseEventSink, ITfLangBarMgr::UnadviseEventSink, UnadviseEventSink, UnadviseEventSink method [Text Services Framework], UnadviseEventSink method [Text Services Framework],ITfLangBarMgr interface, _tsf_itflangbarmgr_unadviseeventsink_ref, ctfutb/ITfLangBarMgr::UnadviseEventSink, tsf.itflangbarmgr_unadviseeventsink
ms.topic: method
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
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
 - ITfLangBarMgr.UnadviseEventSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarMgr::UnadviseEventSink


## -description




## -parameters




### -param dwCookie [in]

A DWORD value that identifies the advise event sink to uninstall. This value is provided by a previous call to <a href="https://msdn.microsoft.com/8ac607fd-b2c4-4441-8738-c64c25b6c586">ITfLangBarMgr::AdviseEventSink</a>.


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




<a href="https://msdn.microsoft.com/60bd765f-0846-47f5-af1b-bc8e72720841">ITfLangBarMgr</a>



<a href="https://msdn.microsoft.com/8ac607fd-b2c4-4441-8738-c64c25b6c586">ITfLangBarMgr::AdviseEventSink
      </a>



<a href="https://msdn.microsoft.com/fd43b4c3-80bb-4118-a880-bdea07022c95">Thread Manager</a>
 

 


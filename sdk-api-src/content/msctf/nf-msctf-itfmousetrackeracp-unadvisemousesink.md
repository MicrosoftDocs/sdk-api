---
UID: NF:msctf.ITfMouseTrackerACP.UnadviseMouseSink
title: ITfMouseTrackerACP::UnadviseMouseSink
author: windows-sdk-content
description: ITfMouseTrackerACP::UnadviseMouseSink method
old-location: tsf\itfmousetrackeracp_unadvisemousesink.htm
old-project: TSF
ms.assetid: 6c753e09-f67a-45d6-b2f9-c08d5c05c04d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfMouseTrackerACP interface [Text Services Framework],UnadviseMouseSink method, ITfMouseTrackerACP.UnadviseMouseSink, ITfMouseTrackerACP::UnadviseMouseSink, UnadviseMouseSink, UnadviseMouseSink method [Text Services Framework], UnadviseMouseSink method [Text Services Framework],ITfMouseTrackerACP interface, _tsf_itfmousetrackeracp_unadvisemousesink_ref, msctf/ITfMouseTrackerACP::UnadviseMouseSink, tsf.itfmousetrackeracp_unadvisemousesink
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfMouseTrackerACP.UnadviseMouseSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfMouseTrackerACP::UnadviseMouseSink


## -description




## -parameters




### -param dwCookie [in]

Specifies the mouse advise sink identifier. This value is obtained by a call to <a href="https://msdn.microsoft.com/365538cd-0f18-45ce-91c2-ee3255b7fa93">ITfMouseTrackerACP::AdviseMouseSink</a>.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The application does not support mouse event sinks.

</td>
</tr>
</table>
 




## -remarks



The application must release the <a href="https://msdn.microsoft.com/d6e5549e-768d-47af-a553-84430641cda4">ITfMouseSink</a> supplied in the <b>ITfMouseTrackerACP::AdviseMouseSink</b> call associated with <i>dwCookie</i>.




## -see-also




<a href="https://msdn.microsoft.com/d6e5549e-768d-47af-a553-84430641cda4">ITfMouseSink
      </a>



<a href="https://msdn.microsoft.com/6761cf80-60b1-4c3a-8c3f-f040fab60f24">ITfMouseTrackerACP</a>



<a href="https://msdn.microsoft.com/365538cd-0f18-45ce-91c2-ee3255b7fa93">ITfMouseTrackerACP::AdviseMouseSink
      </a>
 

 


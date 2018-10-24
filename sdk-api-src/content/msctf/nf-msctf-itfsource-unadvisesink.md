---
UID: NF:msctf.ITfSource.UnadviseSink
title: ITfSource::UnadviseSink
author: windows-sdk-content
description: ITfSource::UnadviseSink method
old-location: tsf\itfsource_unadvisesink.htm
tech.root: TSF
ms.assetid: e5d40c6f-c8ab-4e53-94d0-a6b475ce7a84
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ITfSource interface [Text Services Framework],UnadviseSink method, ITfSource.UnadviseSink, ITfSource::UnadviseSink, UnadviseSink, UnadviseSink method [Text Services Framework], UnadviseSink method [Text Services Framework],ITfSource interface, _tsf_itfsource_unadvisesink_ref, msctf/ITfSource::UnadviseSink, tsf.itfsource_unadvisesink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfSource.UnadviseSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfSource::UnadviseSink


## -description




## -parameters




### -param dwCookie [in]

A DWORD that identifies the advise sink to uninstall. This value is provided by a previous call to <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a>.


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
The <i>dwCookie</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The advise sink cannot be found.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource</a>



<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink
      </a>
 

 


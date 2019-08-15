---
UID: NF:msctf.ITfRange.GetGravity
title: ITfRange::GetGravity (msctf.h)
author: windows-sdk-content
description: ITfRange::GetGravity method
old-location: tsf\itfrange_getgravity.htm
tech.root: TSF
ms.assetid: 7569b9dd-869f-49a6-ad0f-c2d9b5f0ae70
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetGravity, GetGravity method [Text Services Framework], GetGravity method [Text Services Framework],ITfRange interface, ITfRange interface [Text Services Framework],GetGravity method, ITfRange.GetGravity, ITfRange::GetGravity, _tsf_itfrange_getgravity_ref, msctf/ITfRange::GetGravity, tsf.itfrange_getgravity
ms.topic: method
f1_keywords: 
 - "msctf/ITfRange.GetGravity"
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
 - Msctf.dll
api_name:
 - ITfRange.GetGravity
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfRange::GetGravity


## -description




## -parameters




### -param pgStart [out]

Pointer to a <a href="https://docs.microsoft.com/windows/win32/api/msctf/ne-msctf-tfgravity">TfGravity</a> value that receives the gravity of the start anchor.


### -param pgEnd [out]

Pointer to a <b>TfGravity</b> value that receives the gravity of the end anchor.


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
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TSF/ranges">Anchor Gravity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfrange-setgravity">ITfRange::SetGravity</a>



<a href="https://docs.microsoft.com/windows/win32/api/msctf/ne-msctf-tfgravity">TfGravity</a>
 

 


---
UID: NF:msctf.ITfRange.GetGravity
title: ITfRange::GetGravity
author: windows-sdk-content
description: ITfRange::GetGravity method
old-location: tsf\itfrange_getgravity.htm
old-project: TSF
ms.assetid: 7569b9dd-869f-49a6-ad0f-c2d9b5f0ae70
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetGravity, GetGravity method [Text Services Framework], GetGravity method [Text Services Framework],ITfRange interface, ITfRange interface [Text Services Framework],GetGravity method, ITfRange.GetGravity, ITfRange::GetGravity, _tsf_itfrange_getgravity_ref, msctf/ITfRange::GetGravity, tsf.itfrange_getgravity
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfRange::GetGravity


## -description




## -parameters




### -param pgStart [out]

Pointer to a <a href="https://msdn.microsoft.com/844925e7-4c3e-41e7-b560-586c85530cb4">TfGravity</a> value that receives the gravity of the start anchor.


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




<a href="https://msdn.microsoft.com/en-us/library/ms629023(v=VS.85).aspx">Anchor Gravity</a>



<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a>



<a href="https://msdn.microsoft.com/f8be0458-cd14-471d-a138-0730f87374e0">ITfRange::SetGravity</a>



<a href="https://msdn.microsoft.com/844925e7-4c3e-41e7-b560-586c85530cb4">TfGravity</a>
 

 


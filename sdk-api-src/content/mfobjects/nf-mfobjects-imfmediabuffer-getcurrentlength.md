---
UID: NF:mfobjects.IMFMediaBuffer.GetCurrentLength
title: IMFMediaBuffer::GetCurrentLength (mfobjects.h)
description: Retrieves the length of the valid data in the buffer.helpviewer_keywords: ["772e3e6c-0616-41f6-a681-d76da97d85fb","GetCurrentLength","GetCurrentLength method [Media Foundation]","GetCurrentLength method [Media Foundation]","IMFMediaBuffer interface","IMFMediaBuffer interface [Media Foundation]","GetCurrentLength method","IMFMediaBuffer.GetCurrentLength","IMFMediaBuffer::GetCurrentLength","mf.imfmediabuffer_getcurrentlength","mfobjects/IMFMediaBuffer::GetCurrentLength"]
old-location: mf\imfmediabuffer_getcurrentlength.htm
tech.root: medfound
ms.assetid: 772e3e6c-0616-41f6-a681-d76da97d85fb
ms.date: 12/05/2018
ms.keywords: 772e3e6c-0616-41f6-a681-d76da97d85fb, GetCurrentLength, GetCurrentLength method [Media Foundation], GetCurrentLength method [Media Foundation],IMFMediaBuffer interface, IMFMediaBuffer interface [Media Foundation],GetCurrentLength method, IMFMediaBuffer.GetCurrentLength, IMFMediaBuffer::GetCurrentLength, mf.imfmediabuffer_getcurrentlength, mfobjects/IMFMediaBuffer::GetCurrentLength
f1_keywords:
- mfobjects/IMFMediaBuffer.GetCurrentLength
dev_langs:
- c++
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFMediaBuffer.GetCurrentLength
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaBuffer::GetCurrentLength


## -description



Retrieves the length of the valid data in the buffer.




## -parameters




### -param pcbCurrentLength [out]

Receives the length of the valid data, in bytes. If the buffer does not contain any valid data, the value is zero.


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
</table>
 




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-buffers">Media Buffers</a>
 

 


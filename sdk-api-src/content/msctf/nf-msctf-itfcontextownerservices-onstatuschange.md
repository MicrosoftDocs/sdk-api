---
UID: NF:msctf.ITfContextOwnerServices.OnStatusChange
title: ITfContextOwnerServices::OnStatusChange
author: windows-sdk-content
description: The ITfContextOwnerServices::OnStatusChange method is called by the context owner when the dwDynamicFlags member of the TS_STATUS structure returned by the ITfContextOwner::GetStatus method changes.
old-location: tsf\itfcontextownerservices_onstatuschange.htm
tech.root: TSF
ms.assetid: da450910-d592-49c0-8df7-bc2f4037c4d2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITfContextOwnerServices interface [Text Services Framework],OnStatusChange method, ITfContextOwnerServices.OnStatusChange, ITfContextOwnerServices::OnStatusChange, OnStatusChange, OnStatusChange method [Text Services Framework], OnStatusChange method [Text Services Framework],ITfContextOwnerServices interface, _tsf_itfcontextownerservices_onstatuschange_ref, msctf/ITfContextOwnerServices::OnStatusChange, tsf.itfcontextownerservices_onstatuschange
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
 - ITfContextOwnerServices.OnStatusChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- COM
: 
- msctf.h
: 
- ITfContextOwnerServices.OnStatusChange
: 
---

# ITfContextOwnerServices::OnStatusChange


## -description


The <b>ITfContextOwnerServices::OnStatusChange</b> method is called by the context owner when the <b>dwDynamicFlags</b> member of the <a href="https://msdn.microsoft.com/d27d81f2-8599-4b65-866b-4e8fd2f589f5">TS_STATUS</a> structure returned by the <a href="https://msdn.microsoft.com/ce30ec8a-48fe-4ec7-a7e1-2a0cf084097d">ITfContextOwner::GetStatus</a> method changes.


## -parameters




### -param dwFlags [in]

Specifies the dynamic status flag.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ce30ec8a-48fe-4ec7-a7e1-2a0cf084097d">ITfContextOwner::GetStatus
      </a>



<a href="https://msdn.microsoft.com/fb77bd6a-ae34-4e21-8f09-fc8c6a1ade86">ITfContextOwnerServices</a>



<a href="https://msdn.microsoft.com/d27d81f2-8599-4b65-866b-4e8fd2f589f5">TS_STATUS
      </a>
 

 


---
UID: NF:msctf.ITfClientId.GetClientId
title: ITfClientId::GetClientId
author: windows-sdk-content
description: ITfClientId::GetClientId method
old-location: tsf\itfclientid_getclientid.htm
tech.root: TSF
ms.assetid: 422cff3c-1be5-4b86-bc64-cded6ab64da4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetClientId, GetClientId method [Text Services Framework], GetClientId method [Text Services Framework],ITfClientId interface, ITfClientId interface [Text Services Framework],GetClientId method, ITfClientId.GetClientId, ITfClientId::GetClientId, _tsf_itfclientid_getclientid_ref, msctf/ITfClientId::GetClientId, tsf.itfclientid_getclientid
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
 - ITfClientId.GetClientId
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfClientId::GetClientId


## -description




## -parameters




### -param rclsid [in]

CLSID to obtain the client identifier for.


### -param ptid [out]

Pointer to a <a href="https://msdn.microsoft.com/984dc390-6e15-4491-8c06-77c27c5bdd6f">TfClientId</a> value that receives the client identifier.


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
 




## -remarks



An application obtains its client identifier by calling <a href="https://msdn.microsoft.com/bd9058c0-55b0-4231-a336-7cea4db75c0f">ITfThreadMgr::Activate</a> and a text service receives its client identifier in its <a href="https://msdn.microsoft.com/c5fd6b5c-0a78-4b5b-aad5-0c398798cf30">ITfTextInputProcessor::Activate</a> method. <b>ITfClientId::GetClientId</b> enables TSF objects that do not fit either of these categories to obtain their own client identifier.




## -see-also




<a href="https://msdn.microsoft.com/ccb06ed3-67e2-4e46-8037-ff215ba23601">ITfClientId</a>



<a href="https://msdn.microsoft.com/c5fd6b5c-0a78-4b5b-aad5-0c398798cf30">ITfTextInputProcessor::Activate
      </a>



<a href="https://msdn.microsoft.com/bd9058c0-55b0-4231-a336-7cea4db75c0f">ITfThreadMgr::Activate
      </a>



<a href="https://msdn.microsoft.com/984dc390-6e15-4491-8c06-77c27c5bdd6f">TfClientId
      </a>
 

 


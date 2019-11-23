---
UID: NF:msctf.ITfClientId.GetClientId
title: ITfClientId::GetClientId (msctf.h)

description: ITfClientId::GetClientId method
old-location: tsf\itfclientid_getclientid.htm
tech.root: TSF
ms.assetid: 422cff3c-1be5-4b86-bc64-cded6ab64da4

ms.date: 12/05/2018
ms.keywords: GetClientId, GetClientId method [Text Services Framework], GetClientId method [Text Services Framework],ITfClientId interface, ITfClientId interface [Text Services Framework],GetClientId method, ITfClientId.GetClientId, ITfClientId::GetClientId, _tsf_itfclientid_getclientid_ref, msctf/ITfClientId::GetClientId, tsf.itfclientid_getclientid
ms.topic: method
f1_keywords: 
 - "msctf/ITfClientId.GetClientId"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfClientId::GetClientId


## -description




## -parameters




### -param rclsid [in]

CLSID to obtain the client identifier for.


### -param ptid [out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/TSF/tfclientid">TfClientId</a> value that receives the client identifier.


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



An application obtains its client identifier by calling <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-activate">ITfThreadMgr::Activate</a> and a text service receives its client identifier in its <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate">ITfTextInputProcessor::Activate</a> method. <b>ITfClientId::GetClientId</b> enables TSF objects that do not fit either of these categories to obtain their own client identifier.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfclientid">ITfClientId</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate">ITfTextInputProcessor::Activate
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-activate">ITfThreadMgr::Activate
      </a>



<a href="https://docs.microsoft.com/windows/desktop/TSF/tfclientid">TfClientId
      </a>
 

 


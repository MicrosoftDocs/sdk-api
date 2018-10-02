---
UID: NF:msctf.ITfThreadMgr.EnumFunctionProviders
title: ITfThreadMgr::EnumFunctionProviders
author: windows-sdk-content
description: ITfThreadMgr::EnumFunctionProviders method
old-location: tsf\itfthreadmgr_enumfunctionproviders.htm
tech.root: TSF
ms.assetid: 6581cd4d-75ad-4a2c-a919-8e2eed6b3939
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: EnumFunctionProviders, EnumFunctionProviders method [Text Services Framework], EnumFunctionProviders method [Text Services Framework],ITfThreadMgr interface, ITfThreadMgr interface [Text Services Framework],EnumFunctionProviders method, ITfThreadMgr.EnumFunctionProviders, ITfThreadMgr::EnumFunctionProviders, _tsf_itfthreadmgr_enumfunctionproviders_ref, msctf/ITfThreadMgr::EnumFunctionProviders, tsf.itfthreadmgr_enumfunctionproviders
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
 - Msctf.dll
api_name:
 - ITfThreadMgr.EnumFunctionProviders
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfThreadMgr::EnumFunctionProviders


## -description




## -parameters




### -param ppEnum [out]

Address of a <a href="https://msdn.microsoft.com/21e2f1c8-926e-4e53-b8d1-aecc2d1a97cb">IEnumTfFunctionProviders</a> interface that receives the function provider enumerator.


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
<i>ppEnum</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

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
 




## -remarks



The enumerator only contains the registered function providers. The enumerator will not contain the predefined function providers as described in <a href="https://msdn.microsoft.com/b320790a-4b54-4475-97e6-e59f083cfc09">ITfThreadMgr::GetFunctionProvider</a>.

A function provider registers itself by calling the TSF manager <a href="https://msdn.microsoft.com/d9231f36-24c4-4d46-97e7-518f5fcc1ce2">ITfSourceSingle::AdviseSingleSink</a> method with IID_ITfFunctionProvider.




## -see-also




<a href="https://msdn.microsoft.com/21e2f1c8-926e-4e53-b8d1-aecc2d1a97cb">IEnumTfFunctionProviders
      </a>



<a href="https://msdn.microsoft.com/d9231f36-24c4-4d46-97e7-518f5fcc1ce2">ITfSourceSingle::AdviseSingleSink
      </a>



<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a>



<a href="https://msdn.microsoft.com/b320790a-4b54-4475-97e6-e59f083cfc09">ITfThreadMgr::GetFunctionProvider
      </a>
 

 


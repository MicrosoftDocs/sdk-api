---
UID: NF:msctf.ITfThreadMgr2.EnumFunctionProviders
title: ITfThreadMgr2::EnumFunctionProviders
author: windows-sdk-content
description: Obtains an enumerator for all of the function providers registered for the calling thread.
old-location: tsf\itfthreadmgr2_enumfunctionproviders.htm
tech.root: TSF
ms.assetid: 0F28BDFD-4CD8-4D50-92D9-6A60B80122B2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EnumFunctionProviders, EnumFunctionProviders method [Text Services Framework], EnumFunctionProviders method [Text Services Framework],ITfThreadMgr2 interface, ITfThreadMgr2 interface [Text Services Framework],EnumFunctionProviders method, ITfThreadMgr2.EnumFunctionProviders, ITfThreadMgr2::EnumFunctionProviders, msctf/ITfThreadMgr2::EnumFunctionProviders, tsf.itfthreadmgr2_enumfunctionproviders
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.h
api_name:
 - ITfThreadMgr2.EnumFunctionProviders
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- msctf.h
: 
- ITfThreadMgr2.EnumFunctionProviders
: 
---

# ITfThreadMgr2::EnumFunctionProviders


## -description


Obtains an enumerator for all of the function providers registered for the calling thread.


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



The enumerator only contains the registered function providers. The enumerator will not contain the predefined function providers as described in <a href="https://msdn.microsoft.com/4B2B2098-ECA1-454F-8F7F-978893C466F7">GetFunctionProvider</a>.

A function provider registers itself by calling the TSF manager <a href="https://msdn.microsoft.com/d9231f36-24c4-4d46-97e7-518f5fcc1ce2">ITfSourceSingle::AdviseSingleSink</a> method with IID_ITfFunctionProvider.




## -see-also




<a href="https://msdn.microsoft.com/B80A0DBA-349A-450D-BD9D-14BD36308590">ITfThreadMgr2</a>
 

 


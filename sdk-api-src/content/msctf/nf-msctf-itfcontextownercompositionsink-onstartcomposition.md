---
UID: NF:msctf.ITfContextOwnerCompositionSink.OnStartComposition
title: ITfContextOwnerCompositionSink::OnStartComposition (msctf.h)
author: windows-sdk-content
description: ITfContextOwnerCompositionSink::OnStartComposition method
old-location: tsf\itfcontextownercompositionsink_onstartcomposition.htm
tech.root: TSF
ms.assetid: 18356eda-42b1-4b29-8fd8-cff4a3f6d234
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfContextOwnerCompositionSink interface [Text Services Framework],OnStartComposition method, ITfContextOwnerCompositionSink.OnStartComposition, ITfContextOwnerCompositionSink::OnStartComposition, OnStartComposition, OnStartComposition method [Text Services Framework], OnStartComposition method [Text Services Framework],ITfContextOwnerCompositionSink interface, _tsf_itfcontextownercompositionsink_onstartcomposition_ref, msctf/ITfContextOwnerCompositionSink::OnStartComposition, tsf.itfcontextownercompositionsink_onstartcomposition
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
req.dll: Msimtf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msimtf.dll
api_name:
 - ITfContextOwnerCompositionSink.OnStartComposition
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfContextOwnerCompositionSink::OnStartComposition


## -description




## -parameters




### -param pComposition [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcompositionview">ITfCompositionView</a> object that represents the new composition.


### -param pfOk [out]

Pointer to a <b>BOOL</b> value that receives a value that allows or denies the new composition. Receives a nonzero value to allow the composition or zero to deny the composition.


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




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcompositionview">ITfCompositionView
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontextownercompositionsink">ITfContextOwnerCompositionSink</a>
 

 


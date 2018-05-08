---
UID: NF:msctf.ITfContextOwnerCompositionSink.OnStartComposition
title: ITfContextOwnerCompositionSink::OnStartComposition
author: windows-driver-content
description: ITfContextOwnerCompositionSink::OnStartComposition method
old-location: tsf\itfcontextownercompositionsink_onstartcomposition.htm
old-project: TSF
ms.assetid: 18356eda-42b1-4b29-8fd8-cff4a3f6d234
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfContextOwnerCompositionSink interface [Text Services Framework],OnStartComposition method, ITfContextOwnerCompositionSink.OnStartComposition, ITfContextOwnerCompositionSink::OnStartComposition, OnStartComposition, OnStartComposition method [Text Services Framework], OnStartComposition method [Text Services Framework],ITfContextOwnerCompositionSink interface, _tsf_itfcontextownercompositionsink_onstartcomposition_ref, msctf/ITfContextOwnerCompositionSink::OnStartComposition, tsf.itfcontextownercompositionsink_onstartcomposition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msimtf.dll
api_name:
-	ITfContextOwnerCompositionSink.OnStartComposition
product: Windows
targetos: Windows
req.lib: 
req.dll: Msimtf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfContextOwnerCompositionSink::OnStartComposition


## -description




## -parameters




### -param pComposition [in]

Pointer to an <a href="https://msdn.microsoft.com/1c8aac3e-384e-402e-aae8-11e240083603">ITfCompositionView</a> object that represents the new composition.


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




<a href="https://msdn.microsoft.com/1c8aac3e-384e-402e-aae8-11e240083603">ITfCompositionView
      </a>



<a href="https://msdn.microsoft.com/4fea0a48-df5f-4f34-a3ea-d52883f6f8b1">ITfContextOwnerCompositionSink</a>
 

 


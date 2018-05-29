---
UID: NF:msctf.ITfContextComposition.FindComposition
title: ITfContextComposition::FindComposition
author: windows-sdk-content
description: ITfContextComposition::FindComposition method
old-location: tsf\itfcontextcomposition_findcomposition.htm
old-project: TSF
ms.assetid: f5a7bd54-3b8f-44fd-ae6e-1415cc69c49e
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: FindComposition, FindComposition method [Text Services Framework], FindComposition method [Text Services Framework],ITfContextComposition interface, ITfContextComposition interface [Text Services Framework],FindComposition method, ITfContextComposition.FindComposition, ITfContextComposition::FindComposition, _tsf_itfcontextcomposition_findcomposition_ref, msctf/ITfContextComposition::FindComposition, tsf.itfcontextcomposition_findcomposition
ms.prod: windows
ms.technology: windows-sdk
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
-	Msctf.dll
api_name:
-	ITfContextComposition.FindComposition
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfContextComposition::FindComposition


## -description




## -parameters




### -param ecRead [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param pTestRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> object that specifies the range to search. This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the enumerator will contain all compositions in the edit context.


### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/d842b367-a605-4ed0-887d-89dfcf6893a6">IEnumITfCompositionView</a> interface pointer that receives the enumerator object.


## -returns



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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The enumerator object cannot be initialized.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The enumerator object cannot be created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context object is not on a document stack.

</td>
</tr>
</table>
 

The edit context identified by <i>ecRead</i> does not have a read-only lock.




## -see-also




<a href="https://msdn.microsoft.com/d842b367-a605-4ed0-887d-89dfcf6893a6">
        IEnumITfCompositionView
      </a>



<a href="https://msdn.microsoft.com/cf02c50c-dca8-47ad-b8ff-0fa3884db674">ITfContextComposition</a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">
        ITfRange
      </a>
 

 


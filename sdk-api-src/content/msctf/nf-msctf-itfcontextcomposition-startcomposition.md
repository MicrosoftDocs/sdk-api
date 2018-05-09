---
UID: NF:msctf.ITfContextComposition.StartComposition
title: ITfContextComposition::StartComposition
author: windows-driver-content
description: ITfContextComposition::StartComposition method
old-location: tsf\itfcontextcomposition_startcomposition.htm
old-project: TSF
ms.assetid: aab84e6c-39c7-438e-b4f0-1d174473aa02
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: ITfContextComposition interface [Text Services Framework],StartComposition method, ITfContextComposition.StartComposition, ITfContextComposition::StartComposition, StartComposition, StartComposition method [Text Services Framework], StartComposition method [Text Services Framework],ITfContextComposition interface, _tsf_itfcontextcomposition_startcomposition_ref, msctf/ITfContextComposition::StartComposition, tsf.itfcontextcomposition_startcomposition
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
-	Msctf.dll
api_name:
-	ITfContextComposition.StartComposition
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfContextComposition::StartComposition


## -description




## -parameters




### -param ecWrite [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param pCompositionRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> object that specifies the text that the composition initially covers.


### -param pSink [in]

Pointer to an <a href="https://msdn.microsoft.com/17d5eab5-a308-40a5-823a-f176508dda71">ITfCompositionSink</a> object that receives composition event notifications. This parameter is optional and can be <b>NULL</b>. If supplied, the object is released when the composition is terminated.


### -param ppComposition [out]

Pointer to an <a href="https://msdn.microsoft.com/b1eb5782-13e3-4cbb-8c37-ce7219d1e838">ITfComposition</a> interface pointer that receives the new composition object. This parameter receives <b>NULL</b> if the context owner rejects the composition.


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
The method was successful. If the context owner composition advise sink rejects the composition, <i>ppComposition</i> is set to <b>NULL</b>.

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
The composition object cannot be created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method was called within another composition operation.

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
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit context identified by <i>ecWrite</i> does not have a read/write lock.

</td>
</tr>
</table>
 




## -remarks



If the context owner has installed an context owner composition advise sink, the <a href="https://msdn.microsoft.com/18356eda-42b1-4b29-8fd8-cff4a3f6d234">ITfContextOwnerCompositionSink::OnStartComposition</a> method is called. If the advise sink rejects the new composition, this method returns S_OK but <i>ppComposition</i> is set to <b>NULL</b>.

Any text covered by <i>pCompositionRange</i> receives the GUID_PROP_COMPOSING property.




## -see-also




<a href="https://msdn.microsoft.com/b1eb5782-13e3-4cbb-8c37-ce7219d1e838">
        ITfComposition
      </a>



<a href="https://msdn.microsoft.com/17d5eab5-a308-40a5-823a-f176508dda71">
        ITfCompositionSink
      </a>



<a href="https://msdn.microsoft.com/cf02c50c-dca8-47ad-b8ff-0fa3884db674">ITfContextComposition</a>



<a href="https://msdn.microsoft.com/18356eda-42b1-4b29-8fd8-cff4a3f6d234">
        ITfContextOwnerCompositionSink::OnStartComposition
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">
        ITfRange
      </a>
 

 


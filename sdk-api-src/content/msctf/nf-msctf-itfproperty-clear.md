---
UID: NF:msctf.ITfProperty.Clear
title: ITfProperty::Clear
author: windows-sdk-content
description: ITfProperty::Clear method
old-location: tsf\itfproperty_clear.htm
tech.root: TSF
ms.assetid: bbfbbe0d-bea7-4c46-8b9c-6b607a761f48
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: Clear, Clear method [Text Services Framework], Clear method [Text Services Framework],ITfProperty interface, ITfProperty interface [Text Services Framework],Clear method, ITfProperty.Clear, ITfProperty::Clear, _tsf_itfproperty_clear_ref, msctf/ITfProperty::Clear, tsf.itfproperty_clear
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
 - Msctf.dll
api_name:
 - ITfProperty.Clear
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfProperty::Clear


## -description




## -parameters




### -param ec [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> interface that contains the range that the property is cleared for. If this parameter is <b>NULL</b>, all values for this property over the entire edit context are cleared.


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
<i>pRange</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit context identified by <i>ec</i> does not have a read/write lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
The edit context is read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOTOWNEDRANGE</b></dt>
</dl>
</td>
<td width="60%">
The TSF manager does not own the range.

</td>
</tr>
</table>
 




## -remarks



It is not necessary to call this method when a context is about to be destroyed. The TSF manager will clear all properties when the context is removed from the context stack.




## -see-also




<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">ITfProperty</a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 


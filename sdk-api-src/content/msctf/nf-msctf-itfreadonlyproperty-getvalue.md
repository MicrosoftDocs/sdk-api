---
UID: NF:msctf.ITfReadOnlyProperty.GetValue
title: ITfReadOnlyProperty::GetValue
author: windows-sdk-content
description: ITfReadOnlyProperty::GetValue method
old-location: tsf\itfreadonlyproperty_getvalue.htm
tech.root: TSF
ms.assetid: c82ef360-e0b1-4e1a-b839-36b8e9c52347
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetValue, GetValue method [Text Services Framework], GetValue method [Text Services Framework],ITfReadOnlyProperty interface, ITfReadOnlyProperty interface [Text Services Framework],GetValue method, ITfReadOnlyProperty.GetValue, ITfReadOnlyProperty::GetValue, _tsf_itfreadonlyproperty_getvalue_ref, msctf/ITfReadOnlyProperty::GetValue, tsf.itfreadonlyproperty_getvalue
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
 - ITfReadOnlyProperty.GetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfReadOnlyProperty::GetValue


## -description




## -parameters




### -param ec [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> interface that specifies the range to obtain the property for.


### -param pvarValue [out]

Pointer to a <b>VARIANT</b> value that receives the property value. The data type and contents of this value is defined by the property owner and must be recognized by the caller in order to use this value. The caller must release this data, when it is no longer required, by passing this value to the <b>VariantClear</b> API.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The range is not covered by the property or the range contains more than one property value. <i>pvarValue</i> receives a VT_EMPTY value.

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
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit context identified by <i>ec</i> does not have a read-only or read/write lock.

</td>
</tr>
</table>
 




## -remarks



If the property has no value over <i>pRange</i>, <i>pRange</i> contains more than one value for the property or the property does not completely cover <i>pRange</i>, <i>pvarValue</i> receives a VT_EMPTY value and the method returns S_FALSE.

<pre class="syntax" xml:space="preserve"><code>
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
    range--&gt;||&lt;-
</code></pre>
<pre class="syntax" xml:space="preserve"><code>
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
    range--&gt;|    |&lt;-
</code></pre>
<pre class="syntax" xml:space="preserve"><code>
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
    range--&gt;|             |&lt;-
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a>



<a href="https://msdn.microsoft.com/f4021a3d-6b86-469f-8943-770e7ef0cf99">ITfReadOnlyProperty</a>
 

 


---
UID: NF:msctf.ITfDisplayAttributeProvider.EnumDisplayAttributeInfo
title: ITfDisplayAttributeProvider::EnumDisplayAttributeInfo
author: windows-driver-content
description: ITfDisplayAttributeProvider::EnumDisplayAttributeInfo method
old-location: tsf\itfdisplayattributeprovider_enumdisplayattributeinfo.htm
old-project: TSF
ms.assetid: 1a19de91-ad79-4c75-956b-5f5de6700cbe
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: EnumDisplayAttributeInfo, EnumDisplayAttributeInfo method [Text Services Framework], EnumDisplayAttributeInfo method [Text Services Framework],ITfDisplayAttributeProvider interface, ITfDisplayAttributeProvider interface [Text Services Framework],EnumDisplayAttributeInfo method, ITfDisplayAttributeProvider.EnumDisplayAttributeInfo, ITfDisplayAttributeProvider::EnumDisplayAttributeInfo, _tsf_itfdisplayattributeprovider_enumdisplayattributeinfo_ref, msctf/ITfDisplayAttributeProvider::EnumDisplayAttributeInfo, tsf.itfdisplayattributeprovider_enumdisplayattributeinfo
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
-	imjpcic.dll
api_name:
-	ITfDisplayAttributeProvider.EnumDisplayAttributeInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Imjpcic.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfDisplayAttributeProvider::EnumDisplayAttributeInfo


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/b222deb8-22dd-44c3-9ecc-0fb379682796">IEnumTfDisplayAttributeInfo</a> interface pointer that receives the enumerator object. The caller must release this interface when it is no longer required.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b222deb8-22dd-44c3-9ecc-0fb379682796">IEnumTfDisplayAttributeInfo
      </a>



<a href="https://msdn.microsoft.com/c0346d5e-d4a2-4c72-90be-de5ff1681acd">ITfDisplayAttributeProvider</a>
 

 


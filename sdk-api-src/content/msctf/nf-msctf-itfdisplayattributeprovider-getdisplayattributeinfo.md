---
UID: NF:msctf.ITfDisplayAttributeProvider.GetDisplayAttributeInfo
title: ITfDisplayAttributeProvider::GetDisplayAttributeInfo (msctf.h)
author: windows-sdk-content
description: ITfDisplayAttributeProvider::GetDisplayAttributeInfo method
old-location: tsf\itfdisplayattributeprovider_getdisplayattributeinfo.htm
tech.root: TSF
ms.assetid: 2081f1b4-45b4-43bd-ba20-392a5ad0a30e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDisplayAttributeInfo, GetDisplayAttributeInfo method [Text Services Framework], GetDisplayAttributeInfo method [Text Services Framework],ITfDisplayAttributeProvider interface, ITfDisplayAttributeProvider interface [Text Services Framework],GetDisplayAttributeInfo method, ITfDisplayAttributeProvider.GetDisplayAttributeInfo, ITfDisplayAttributeProvider::GetDisplayAttributeInfo, _tsf_itfdisplayattributeprovider_getdisplayattributeinfo_ref, msctf/ITfDisplayAttributeProvider::GetDisplayAttributeInfo, tsf.itfdisplayattributeprovider_getdisplayattributeinfo
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
req.dll: Imjpcic.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imjpcic.dll
api_name:
 - ITfDisplayAttributeProvider.GetDisplayAttributeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfDisplayAttributeProvider::GetDisplayAttributeInfo


## -description




## -parameters




### -param guid [in]

Contains a GUID value that identifies the display attribute to obtain the display attribute information object for. The text service must publish these values and what they indicate. This identifier can also be obtained by enumerating the display attributes for a range of text.


### -param ppInfo [out]

Pointer to an <a href="https://msdn.microsoft.com/7f590ecf-06e9-42da-ba40-4364296ae594">ITfDisplayAttributeInfo</a> interface pointer that receives the display attribute information object.


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
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9e9a72a8-ea9b-4438-992c-5a7db64f7d82">ITfCategoryMgr::RegisterCategory
      </a>



<a href="https://msdn.microsoft.com/7f590ecf-06e9-42da-ba40-4364296ae594">ITfDisplayAttributeInfo
      </a>



<a href="https://msdn.microsoft.com/c0346d5e-d4a2-4c72-90be-de5ff1681acd">ITfDisplayAttributeProvider</a>



<a href="https://msdn.microsoft.com/5809f5b8-0396-4abd-b5fe-61ecc8cd0914">Providing Display Attributes</a>
 

 


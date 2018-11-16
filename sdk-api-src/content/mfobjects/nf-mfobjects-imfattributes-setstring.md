---
UID: NF:mfobjects.IMFAttributes.SetString
title: IMFAttributes::SetString
author: windows-sdk-content
description: Associates a wide-character string with a key.
old-location: mf\imfattributes_setstring.htm
tech.root: medfound
ms.assetid: 51d2a2a0-92cb-49e0-b4a9-7201e9d92322
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 51d2a2a0-92cb-49e0-b4a9-7201e9d92322, IMFAttributes interface [Media Foundation],SetString method, IMFAttributes.SetString, IMFAttributes::SetString, SetString, SetString method [Media Foundation], SetString method [Media Foundation],IMFAttributes interface, mf.imfattributes_setstring, mfobjects/IMFAttributes::SetString
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAttributes.SetString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfobjects.h
: 
- IMFAttributes.SetString
: 
---

# IMFAttributes::SetString


## -description



Associates a wide-character string with a key.




## -parameters




### -param guidKey [in]

GUID that identifies the value to set. If this key already exists, the method overwrites the old value.


### -param wszValue [in]

Null-terminated wide-character string to associate with this key. The method stores a copy of the string.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



To retrieve the string, call <a href="https://msdn.microsoft.com/756d8fba-d372-46f9-8035-f657d7ff133f">IMFAttributes::GetString</a> or <a href="https://msdn.microsoft.com/550a3035-ea16-4784-8f69-9522259bb338">IMFAttributes::GetAllocatedString</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>
 

 


---
UID: NF:mfobjects.IMFAttributes.SetDouble
title: IMFAttributes::SetDouble
author: windows-sdk-content
description: Associates a double value with a key.
old-location: mf\imfattributes_setdouble.htm
tech.root: medfound
ms.assetid: bb58f35e-0fca-4b19-9976-de2140e6ebc0
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFAttributes interface [Media Foundation],SetDouble method, IMFAttributes.SetDouble, IMFAttributes::SetDouble, SetDouble, SetDouble method [Media Foundation], SetDouble method [Media Foundation],IMFAttributes interface, bb58f35e-0fca-4b19-9976-de2140e6ebc0, mf.imfattributes_setdouble, mfobjects/IMFAttributes::SetDouble
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
 - IMFAttributes.SetDouble
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAttributes::SetDouble


## -description



Associates a <b>double</b> value with a key.




## -parameters




### -param guidKey [in]

GUID that identifies the value to set. If this key already exists, the method overwrites the old value.


### -param fValue [in]

New value for this key.


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



To retrieve the double value, call <a href="https://msdn.microsoft.com/650a5f7f-609f-477b-8834-ff66ca3a9ca3">IMFAttributes::GetDouble</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>
 

 


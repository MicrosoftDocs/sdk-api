---
UID: NF:mfobjects.IMFAttributes.SetUINT32
title: IMFAttributes::SetUINT32
author: windows-sdk-content
description: Associates a UINT32 value with a key.
old-location: mf\imfattributes_setuint32.htm
old-project: medfound
ms.assetid: 9c30fd56-719f-4831-8fbf-cefcf9d72709
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 9c30fd56-719f-4831-8fbf-cefcf9d72709, IMFAttributes interface [Media Foundation],SetUINT32 method, IMFAttributes.SetUINT32, IMFAttributes::SetUINT32, SetUINT32, SetUINT32 method [Media Foundation], SetUINT32 method [Media Foundation],IMFAttributes interface, mf.imfattributes_setuint32, mfobjects/IMFAttributes::SetUINT32
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.redist: 
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
tech.root: 
req.typenames: MF_FILE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAttributes.SetUINT32
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFAttributes::SetUINT32


## -description



Associates a <b>UINT32</b> value with a key.




## -parameters




### -param guidKey [in]

GUID that identifies the value to set. If this key already exists, the method overwrites the old value.


### -param unValue [in]

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



To retrieve the <b>UINT32</b> value, call <a href="https://msdn.microsoft.com/e47495e0-3274-4ce2-9fd3-d2fb2afb7578">IMFAttributes::GetUINT32</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>
 

 


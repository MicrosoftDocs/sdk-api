---
UID: NF:mfobjects.IMFAttributes.SetBlob
title: IMFAttributes::SetBlob
author: windows-driver-content
description: Associates a byte array with a key.
old-location: mf\imfattributes_setblob.htm
old-project: medfound
ms.assetid: 4a2a25a9-4dea-40c8-988c-9e3806c8f31c
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 4a2a25a9-4dea-40c8-988c-9e3806c8f31c, IMFAttributes interface [Media Foundation],SetBlob method, IMFAttributes.SetBlob, IMFAttributes::SetBlob, SetBlob, SetBlob method [Media Foundation], SetBlob method [Media Foundation],IMFAttributes interface, mf.imfattributes_setblob, mfobjects/IMFAttributes::SetBlob
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFAttributes.SetBlob
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFAttributes::SetBlob


## -description



Associates a byte array with a key.




## -parameters




### -param guidKey [in]

GUID that identifies the value to set. If this key already exists, the method overwrites the old value.


### -param pBuf [in]

Pointer to a byte array to associate with this key. The method stores a copy of the array.


### -param cbBufSize [in]

Size of the array, in bytes.


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



To retrieve the byte array, call <a href="https://msdn.microsoft.com/68528db7-90df-4abe-a957-ffb8c3f12cef">IMFAttributes::GetBlob</a> or <a href="https://msdn.microsoft.com/380e0e3a-b5c5-4d31-8793-417262377fef">IMFAttributes::GetAllocatedBlob</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>
 

 


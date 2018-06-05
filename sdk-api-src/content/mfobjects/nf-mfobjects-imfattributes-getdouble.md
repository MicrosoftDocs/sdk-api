---
UID: NF:mfobjects.IMFAttributes.GetDouble
title: IMFAttributes::GetDouble
author: windows-sdk-content
description: Retrieves a double value associated with a key.
old-location: mf\imfattributes_getdouble.htm
old-project: medfound
ms.assetid: 650a5f7f-609f-477b-8834-ff66ca3a9ca3
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 650a5f7f-609f-477b-8834-ff66ca3a9ca3, GetDouble, GetDouble method [Media Foundation], GetDouble method [Media Foundation],IMFAttributes interface, IMFActivate.GetDouble, IMFAttributes interface [Media Foundation],GetDouble method, IMFAttributes.GetDouble, IMFAttributes::GetDouble, mf.imfattributes_getdouble, mfobjects/IMFAttributes::GetDouble
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
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
-	IMFAttributes.GetDouble
-	IMFActivate.GetDouble
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFAttributes::GetDouble


## -description



Retrieves a <b>double</b> value associated with a key.




## -parameters




### -param guidKey [in]

GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_DOUBLE</b>.


### -param pfValue [out]

Receives a <b>double</b> value. If the key is found and the data type is <b>double</b>, the method copies the value into this parameter. Otherwise, the original value of this parameter is not changed.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified key was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDTYPE</b></dt>
</dl>
</td>
<td width="60%">
The attribute value is not a <b>double</b>.

</td>
</tr>
</table>
 




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/61a9e327-da29-45fd-8a99-e341561826af">MFGetAttributeDouble</a>



<a href="https://msdn.microsoft.com/1844fbe2-0a07-4c0c-9ffe-4c59fc01f793">MF_ATTRIBUTE_TYPE</a>
 

 


---
UID: NF:olectl.OleLoadPicturePath
title: OleLoadPicturePath function
author: windows-sdk-content
description: Creates a new picture object and initializes it from the contents of a stream. This is equivalent to calling OleCreatePictureIndirect(NULL, ...) followed by IPersistStream::Load.
old-location: com\oleloadpicturepath.htm
old-project: com
ms.assetid: 08bad900-815a-4b6d-b977-92d5fdd7d9e8
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: OleLoadPicturePath, OleLoadPicturePath function [COM], _ctrl_OleLoadPicturePath, com.oleloadpicturepath, olectl/OleLoadPicturePath
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: olectl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PARAMDATA, *LPPARAMDATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	OleLoadPicturePath
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OleLoadPicturePath function


## -description


Creates a new picture object and initializes it from the contents of a stream. This is equivalent to calling <a href="https://msdn.microsoft.com/fb021348-07d4-4974-a71e-abb1b8d760c4">OleCreatePictureIndirect(NULL, ...)</a> followed by <a href="https://msdn.microsoft.com/351e1187-9959-4542-8778-925457c3b8e3">IPersistStream::Load</a>.


## -parameters




### -param szURLorPath [in]

The path or URL to the file you want to open.


### -param punkCaller [in]

Points to <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> for COM aggregation.


### -param dwReserved [in]

Reserved.


### -param clrReserved [in]

The color you want to reserve to be transparent.


### -param riid [in]

Reference to the identifier of the interface describing the type of interface pointer to return in ppvRet.


### -param ppvRet [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvRet</i> contains the requested interface pointer on the storage of the object identified by the moniker. If *<i>ppvRet</i> is non-<b>NULL</b>, this function calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a> on the interface; it is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a>. If an error occurs, *<i>ppvRet</i> is set to <b>NULL</b>.


## -returns



This function supports the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following: 



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
The dialog box was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unable to load picture stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>ppvRet</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the interface specified in <i>riid</i>. 

</td>
</tr>
</table>
 




## -remarks



The stream must be in BMP (bitmap), JPEG, WMF (metafile), ICO (icon), or GIF format.




## -see-also




<a href="https://msdn.microsoft.com/de1847cd-ecc0-4941-9dbc-a60b8ef0b1c1">OleLoadPicture</a>
 

 


---
UID: NF:infotech.IITDatabase.CreateObject
title: IITDatabase::CreateObject
author: windows-sdk-content
description: Creates an unnamed object you can reference in the future through the *pdwObjInstance parameter.
old-location: htmlhelp\iitdatabase_createobject.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitdatabasecreateobject.htm
ms.author: windowssdkdev
ms.date: 10/22/2018
ms.keywords: CreateObject, CreateObject method [HTML Help Workshop], CreateObject method [HTML Help Workshop],IITDatabase interface, IITDatabase interface [HTML Help Workshop],CreateObject method, IITDatabase.CreateObject, IITDatabase::CreateObject, htmlhelp.iitdatabase_createobject, infotech/IITDatabase::CreateObject, refIITDatabaseCreateObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: infotech.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Infotech.h
api_name:
 - IITDatabase.CreateObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- infotech.h
: 
- IITDatabase.CreateObject
: 
---

# IITDatabase::CreateObject


## -description


Creates an unnamed object you can reference in the future through the *<i>pdwObjInstance</i> parameter.




## -parameters




### -param rclsid [in]

Class ID for object.




### -param pdwObjInstance [out]

Identifier for object.




## -returns



This method can return one of these values.

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
The object was successfully created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTINIT</b></dt>
</dl>
</td>
<td width="60%">
The database has not been opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The memory required for internal structures could not be allocated.



</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/16051c95-5fad-43ea-9b85-a4754077dc3c">IITDatabase</a>
 

 


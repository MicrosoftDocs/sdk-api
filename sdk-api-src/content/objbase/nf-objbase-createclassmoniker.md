---
UID: NF:objbase.CreateClassMoniker
title: CreateClassMoniker function
author: windows-sdk-content
description: Creates a class moniker that refers to the specified class.
old-location: com\createclassmoniker.htm
old-project: com
ms.assetid: 9361b2c1-ef26-4225-92ff-e0bef0285bc4
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: CreateClassMoniker, CreateClassMoniker function [COM], _com_CreateClassMoniker, com.createclassmoniker, objbase/CreateClassMoniker
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: COMSD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
api_name:
-	CreateClassMoniker
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CreateClassMoniker function


## -description


Creates a class moniker that refers to the specified class.


## -parameters




### -param rclsid [in]

A reference to the CLSID of the object type to which this moniker binds.


### -param ppmk [out]

The address of an <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>* pointer variable that receives the interface pointer to the new class moniker. On successful return, the function has called <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the moniker and the caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>. When an error occurs, the value of the moniker pointer is <b>NULL</b>.


## -returns



This function can return the following values.

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
The moniker has been created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are invalid.

</td>
</tr>
</table>
 




## -remarks



The class moniker will support the binding to a fresh instance of the class identified by the CLSID in <i>rclsid</i>.





## -see-also




<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>
 

 


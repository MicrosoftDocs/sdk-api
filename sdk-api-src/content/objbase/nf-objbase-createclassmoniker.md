---
UID: NF:objbase.CreateClassMoniker
title: CreateClassMoniker function (objbase.h)
author: windows-sdk-content
description: Creates a class moniker that refers to the specified class.
old-location: com\createclassmoniker.htm
tech.root: com
ms.assetid: 9361b2c1-ef26-4225-92ff-e0bef0285bc4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateClassMoniker, CreateClassMoniker function [COM], _com_CreateClassMoniker, com.createclassmoniker, objbase/CreateClassMoniker
ms.topic: function
f1_keywords: 
 - "objbase/CreateClassMoniker"
dev_langs:
 - c++
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - CreateClassMoniker
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateClassMoniker function


## -description


Creates a class moniker that refers to the specified class.


## -parameters




### -param rclsid [in]

A reference to the CLSID of the object type to which this moniker binds.


### -param ppmk [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>* pointer variable that receives the interface pointer to the new class moniker. On successful return, the function has called <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the moniker and the caller is responsible for calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. When an error occurs, the value of the moniker pointer is <b>NULL</b>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>
 

 


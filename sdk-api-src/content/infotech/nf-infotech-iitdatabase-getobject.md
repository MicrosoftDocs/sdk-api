---
UID: NF:infotech.IITDatabase.GetObject
title: IITDatabase::GetObject
author: windows-sdk-content
description: Retrieves a specified IUnknown-based interface on the object identified by the dwObjInstance parameter.
old-location: htmlhelp\iitdatabase_getobject.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitdatabasegetobject.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetObject, GetObject method [HTML Help Workshop], GetObject method [HTML Help Workshop],IITDatabase interface, IITDatabase interface [HTML Help Workshop],GetObject method, IITDatabase.GetObject, IITDatabase::GetObject, htmlhelp.iitdatabase_getobject, infotech/IITDatabase::GetObject, refIITDatabaseGetObject
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
 - IITDatabase.GetObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IITDatabase::GetObject


## -description


Retrieves a specified <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>-based interface on the object identified by the <i>dwObjInstance</i> parameter.




## -parameters




### -param dwObjInstance [in]

Identifier for object.




### -param riid [in]


### -param ppvObj [out]

Interface ID requested.




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
The operation completed successfully.

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
 

 


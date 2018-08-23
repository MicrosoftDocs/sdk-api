---
UID: NF:infotech.IITDatabase.GetObject
title: IITDatabase::GetObject
author: windows-sdk-content
description: Retrieves a specified IUnknown-based interface on the object identified by the dwObjInstance parameter.
old-location: htmlhelp\iitdatabase_getobject.htm
old-project: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitdatabasegetobject.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetObject, GetObject method [HTML Help Workshop], GetObject method [HTML Help Workshop],IITDatabase interface, IITDatabase interface [HTML Help Workshop],GetObject method, IITDatabase.GetObject, IITDatabase::GetObject, htmlhelp.iitdatabase_getobject, infotech/IITDatabase::GetObject, refIITDatabaseGetObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: infotech.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: POLICY_ELEMENT, *PPOLICY_ELEMENT
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
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/en-us/library/ms670034(v=VS.85).aspx">IITDatabase</a>
 

 


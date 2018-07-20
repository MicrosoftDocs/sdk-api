---
UID: NF:objidl.IDataObject.DUnadvise
title: IDataObject::DUnadvise
author: windows-sdk-content
description: Destroys a notification connection that had been previously set up.
old-location: com\idataobject_dunadvise.htm
old-project: com
ms.assetid: bb9ae4c5-8655-4553-9a1c-ce52c6c86299
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: DUnadvise, DUnadvise method [COM], DUnadvise method [COM],IDataObject interface, IDataObject interface [COM],DUnadvise method, IDataObject.DUnadvise, IDataObject::DUnadvise, _ole_idataobject_dunadvise, com.idataobject_dunadvise, objidl/IDataObject::DUnadvise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IDataObject.DUnadvise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IDataObject::DUnadvise


## -description


Destroys a notification connection that had been previously set up.


## -parameters




### -param dwConnection [in]

A token that specifies the connection to be removed. Use the value returned by <a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a> when the connection was originally established.


## -returns



This method returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The specified value for <i>dwConnection</i> is not a valid connection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_ADVISENOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> implementation does not support notification.

</td>
</tr>
</table>
 




## -remarks



This methods destroys a notification created with a call to the <a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a> method.

If the advisory connection being deleted was initially set up by delegating the <a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a> call to <a href="https://msdn.microsoft.com/3b72a50b-a18f-4ec0-9d1d-52b07eb84faf">IDataAdviseHolder::Advise</a>, you must delegate this call to <a href="https://msdn.microsoft.com/baeb29fd-1dd2-4320-911d-b271b2250184">IDataAdviseHolder::Unadvise</a> to delete it.




## -see-also




<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>
 

 


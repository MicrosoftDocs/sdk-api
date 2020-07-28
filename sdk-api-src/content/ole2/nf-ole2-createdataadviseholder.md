---
UID: NF:ole2.CreateDataAdviseHolder
title: CreateDataAdviseHolder function (ole2.h)
description: Retrieves a pointer to the OLE implementation of IDataAdviseHolder on the data advise holder object.
helpviewer_keywords: ["CreateDataAdviseHolder","CreateDataAdviseHolder function [COM]","_ole_CreateDataAdviseHolder","com.createdataadviseholder","ole2/CreateDataAdviseHolder"]
old-location: com\createdataadviseholder.htm
tech.root: com
ms.assetid: a2114f2f-106a-4a26-ba94-1b40af90a0f3
ms.date: 12/05/2018
ms.keywords: CreateDataAdviseHolder, CreateDataAdviseHolder function [COM], _ole_CreateDataAdviseHolder, com.createdataadviseholder, ole2/CreateDataAdviseHolder
f1_keywords:
- ole2/CreateDataAdviseHolder
dev_langs:
- c++
req.header: ole2.h
req.include-header: ObjBase.h
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
- ext-ms-win-com-ole32-l1-1-3.dll
- Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
- CreateDataAdviseHolder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateDataAdviseHolder function


## -description


Retrieves a pointer to the OLE implementation of <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataadviseholder">IDataAdviseHolder</a> on the data advise holder object.




## -parameters




### -param ppDAHolder [out]

Address of an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataadviseholder">IDataAdviseHolder</a> pointer variable that receives the interface pointer to the new advise holder object.


## -returns



This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

</td>
</tr>
</table>
 




## -remarks



Call <b>CreateDataAdviseHolder</b> in your implementation of <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a> to get a pointer to the OLE implementation of <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataadviseholder">IDataAdviseHolder</a> interface. With this pointer, you can then complete the implementation of <b>IDataObject::DAdvise</b> by calling the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idataadviseholder-advise">IDataAdviseHolder::Advise</a> method, which creates an advisory connection between the calling object and the data object.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataadviseholder">IDataAdviseHolder</a>
 

 


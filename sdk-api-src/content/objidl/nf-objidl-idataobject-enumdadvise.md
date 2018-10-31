---
UID: NF:objidl.IDataObject.EnumDAdvise
title: IDataObject::EnumDAdvise
author: windows-sdk-content
description: Creates an object that can be used to enumerate the current advisory connections.
old-location: com\idataobject_enumdadvise.htm
tech.root: com
ms.assetid: 319637fd-d9b5-4da0-ac92-4c52fa9f5231
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: EnumDAdvise, EnumDAdvise method [COM], EnumDAdvise method [COM],IDataObject interface, IDataObject interface [COM],EnumDAdvise method, IDataObject.EnumDAdvise, IDataObject::EnumDAdvise, _ole_idataobject_enumdadvise, com.idataobject_enumdadvise, objidl/IDataObject::EnumDAdvise
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IDataObject.EnumDAdvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataObject::EnumDAdvise


## -description


Creates an object that can be used to enumerate the current advisory connections.


## -parameters




### -param ppenumAdvise [out]

A pointer to an <a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a> pointer variable that receives the interface pointer to the new enumerator object. If the implementation sets *<i>ppenumAdvise</i> to <b>NULL</b>, there are no connections to advise sinks at this time.


## -returns



This method returns S_OK if the enumerator object is successfully instantiated or there are no connections. Other possible values include the following.

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
Insufficient memory is available for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_ADVISENOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Advisory notifications are not supported by this object.

</td>
</tr>
</table>
 




## -remarks



The enumerator object created by this method implements the <a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a> interface. <b>IEnumSTATDATA</b> permits the enumeration of the data stored in an array of <a href="https://msdn.microsoft.com/f31469b2-4a4a-4da5-9229-38ddd0bcc88e">STATDATA</a> structures. Each of these structures provides information on a single advisory connection, and includes <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> and <a href="https://msdn.microsoft.com/e1ad9c17-e492-4891-bf1d-cbac48ce537a">ADVF</a> information, as well as the pointer to the advise sink and the token representing the connection.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
It is recommended that you use the OLE data advise holder object to handle advisory connections. With the pointer obtained through a call to <a href="https://msdn.microsoft.com/a2114f2f-106a-4a26-ba94-1b40af90a0f3">CreateDataAdviseHolder</a>, implementing <b>IDataObject::EnumDAdvise</b> becomes a simple matter of delegating the call to <a href="https://msdn.microsoft.com/0863d013-6f55-40ce-92d2-68bb0455a911">IDataAdviseHolder::EnumAdvise</a>. This creates the enumerator and supplies the pointer to the OLE implementation of <a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a>. At that point, you can call its methods to enumerate the current advisory connections.




## -see-also




<a href="https://msdn.microsoft.com/0863d013-6f55-40ce-92d2-68bb0455a911">IDataAdviseHolder::EnumAdvise</a>



<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>



<a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a>
 

 


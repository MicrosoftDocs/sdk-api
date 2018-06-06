---
UID: NF:ole2.OleRegEnumFormatEtc
title: OleRegEnumFormatEtc function
author: windows-sdk-content
description: Creates an enumeration object that can be used to enumerate data formats that an OLE object server has registered in the system registry.
old-location: com\oleregenumformatetc.htm
old-project: com
ms.assetid: 6caebc68-a136-40f2-92d8-7f8003c18e5c
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: OleRegEnumFormatEtc, OleRegEnumFormatEtc function [COM], _ole_OleRegEnumFormatEtc, com.oleregenumformatetc, ole2/OleRegEnumFormatEtc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ole2.h
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
tech.root: 
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleRegEnumFormatEtc
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OleRegEnumFormatEtc function


## -description


Creates an enumeration object that can be used to enumerate data formats that an OLE object server has registered in the system registry. An object application or object handler calls this function when it must enumerate those formats. Developers of custom DLL object applications use this function to emulate the behavior of the default object handler.


## -parameters




### -param clsid [in]

CLSID of the class whose formats are being requested.


### -param dwDirection [in]

Indicates whether to enumerate formats that can be passed to <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a> or formats that can be passed to <a href="https://msdn.microsoft.com/7430d12c-ab07-4a9c-a845-4743818afbc7">IDataObject::SetData</a>. Possible values are taken from the enumeration <a href="https://msdn.microsoft.com/395d7511-f491-4d6c-9360-cae7e16e8524">DATADIR</a>.


### -param ppenum [out]

Address of <a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a> pointer variable that receives the interface pointer to the enumeration object.


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
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
There is no CLSID registered for the class object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_READREGDB</b></dt>
</dl>
</td>
<td width="60%">
There was an error reading the registry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_REGDB_KEY</b></dt>
</dl>
</td>
<td width="60%">
The DataFormats/GetSet key is missing from the registry.


</td>
</tr>
</table>
 




## -remarks



Object applications can ask OLE to create an enumeration object for <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structures to enumerate supported data formats in one of two ways. One way is to call <b>OleRegEnumFormatEtc</b>. The other is to return OLE_S_USEREG in response to calls by the default object handler to <a href="https://msdn.microsoft.com/657a7394-4481-4e0c-912d-40a9348caf16">IDataObject::EnumFormatEtc</a>. OLE_S_USEREG instructs the default handler to call <b>OleRegEnumFormatEtc</b>. Because DLL object applications cannot return OLE_S_USEREG, they must call <b>OleRegEnumFormatEtc</b> rather than delegating the job to the object handler. With the supplied <a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a> pointer to the object, you can call the standard enumeration object methods to do the enumeration.



The <b>OleRegEnumFormatEtc</b> function and its sibling functions, <a href="https://msdn.microsoft.com/492a4084-494e-4d78-8f3a-853ec486a2d6">OleRegGetUserType</a>, <a href="https://msdn.microsoft.com/3166955f-4f7a-4904-a7fb-ebdfb8e56baf">OleRegGetMiscStatus</a>, and <a href="https://msdn.microsoft.com/25cd0876-90b6-4fa3-b180-ffa0c3b51497">OleRegEnumVerbs</a>, provide a way for developers of custom DLL object applications to emulate the behavior of OLE's default object handler in getting information about objects from the registry. By using these functions, you avoid the considerable work of writing your own, and the pitfalls inherent in working directly in the registry. In addition, you get future enhancements and optimizations of these functions without having to code them yourself.





## -see-also




<a href="https://msdn.microsoft.com/657a7394-4481-4e0c-912d-40a9348caf16">IDataObject::EnumFormatEtc</a>



<a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a>
 

 


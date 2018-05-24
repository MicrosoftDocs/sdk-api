---
UID: NF:ole2.OleRegGetMiscStatus
title: OleRegGetMiscStatus function
author: windows-driver-content
description: Returns miscellaneous information about the presentation and behaviors supported by the specified CLSID from the registry.
old-location: com\olereggetmiscstatus.htm
old-project: com
ms.assetid: 3166955f-4f7a-4904-a7fb-ebdfb8e56baf
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: OleRegGetMiscStatus, OleRegGetMiscStatus function [COM], _com_OleRegGetMiscStatus, com.olereggetmiscstatus, ole2/OleRegGetMiscStatus
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: QACONTROL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
-	ext-ms-win-com-ole32-l1-1-3.dll
-	Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
-	OleRegGetMiscStatus
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OleRegGetMiscStatus function


## -description


Returns miscellaneous information about the presentation and behaviors supported by the specified CLSID from the registry. 

This function is used by developers of custom DLL object applications to emulate the behavior of the OLE default handler.



## -parameters




### -param clsid [in]

The CLSID of the class for which status information is to be requested.


### -param dwAspect [in]

The presentation aspect of the class for which information is requested. Possible values are taken from the <a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a> enumeration.


### -param pdwStatus [out]

A pointer to the variable that receives the status information.


## -returns



This function can return the standard return value E_OUTOFMEMORY, as well as the following values.

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
The status information was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
No CLSID is registered for the class object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_READREGDB</b></dt>
</dl>
</td>
<td width="60%">
There was an error reading from the registry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_REGDB_KEY</b></dt>
</dl>
</td>
<td width="60%">
The <b>GetMiscStatus</b> key is missing from the registry.


</td>
</tr>
</table>
 




## -remarks



Object applications can ask OLE to get miscellaneous status information in one of two ways. One way is to call <b>OleRegGetMiscStatus</b>. The other is to return OLE_S_USEREG in response to calls by the default object handler to <a href="https://msdn.microsoft.com/0c5e9f73-8eec-48e0-a172-4d3d49e56071">IOleObject::GetMiscStatus</a>. OLE_S_USEREG instructs the default handler to call <b>OleRegGetMiscStatus</b>. Because DLL object applications cannot return OLE_S_USEREG, they must call <b>OleRegGetMiscStatus</b> rather than delegating the job to the object handler.



<b>OleRegGetMiscStatus</b> and its sibling functions, <a href="https://msdn.microsoft.com/492a4084-494e-4d78-8f3a-853ec486a2d6">OleRegGetUserType</a>, <a href="https://msdn.microsoft.com/6caebc68-a136-40f2-92d8-7f8003c18e5c">OleRegEnumFormatEtc</a>, and <a href="https://msdn.microsoft.com/25cd0876-90b6-4fa3-b180-ffa0c3b51497">OleRegEnumVerbs</a>, provide a way for developers of custom DLL object applications to emulate the behavior of OLE's default object handler in getting information about objects from the registry. By using these functions, you avoid the considerable work of writing your own, and the pitfalls inherent in working directly in the registry. In addition, you get future enhancements and optimizations of these functions without having to code them yourself.





## -see-also




<a href="https://msdn.microsoft.com/0c5e9f73-8eec-48e0-a172-4d3d49e56071">IOleObject::GetMiscStatus</a>



<a href="https://msdn.microsoft.com/6caebc68-a136-40f2-92d8-7f8003c18e5c">OleRegEnumFormatEtc</a>



<a href="https://msdn.microsoft.com/25cd0876-90b6-4fa3-b180-ffa0c3b51497">OleRegEnumVerbs</a>



<a href="https://msdn.microsoft.com/492a4084-494e-4d78-8f3a-853ec486a2d6">OleRegGetUserType</a>
 

 


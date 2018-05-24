---
UID: NF:ole2.OleRegGetUserType
title: OleRegGetUserType function
author: windows-driver-content
description: Gets the user type of the specified class from the registry.
old-location: com\olereggetusertype.htm
old-project: com
ms.assetid: 492a4084-494e-4d78-8f3a-853ec486a2d6
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: OleRegGetUserType, OleRegGetUserType function [COM], _com_OleRegGetUserType, com.olereggetusertype, ole2/OleRegGetUserType
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
-	OleRegGetUserType
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OleRegGetUserType function


## -description


Gets the user type of the specified class from the registry. 

Developers of custom DLL object applications use this function to emulate the behavior of the OLE default handler.



## -parameters




### -param clsid [in]

The CLSID of the class for which the user type is to be requested.


### -param dwFormOfType [in]

The form of the user-presentable string. Possible values are taken from the enumeration <a href="https://msdn.microsoft.com/f35dd18a-7fde-4954-8315-bc9bfd933827">USERCLASSTYPE</a>.


### -param pszUserType [out]

A pointer to a string that receives the user type.


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
The user type was returned successfully.

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
The  <b>ProgID</b> = <i>MainUserTypeName</i> and <b>CLSID</b> = <i>MainUserTypeName</i> keys  are missing from the registry.


</td>
</tr>
</table>
 




## -remarks



Object applications can ask OLE to get the user type name of a specified class in one of two ways. One way is to call <b>OleRegGetUserType</b>. The other is to return OLE_S_USEREG in response to calls by the default object handler to <a href="https://msdn.microsoft.com/8ffffa01-d118-4955-84d1-a4659ba9ddc9">IOleObject::GetUserType</a>. OLE_S_USEREG instructs the default handler to call <b>OleRegGetUserType</b>. Because DLL object applications cannot return OLE_S_USEREG, they must call <b>OleRegGetUserType</b>, rather than delegating the job to the object handler.



The <b>OleRegGetUserType</b> function and its sibling functions, <a href="https://msdn.microsoft.com/3166955f-4f7a-4904-a7fb-ebdfb8e56baf">OleRegGetMiscStatus</a>, <a href="https://msdn.microsoft.com/6caebc68-a136-40f2-92d8-7f8003c18e5c">OleRegEnumFormatEtc</a>, and <a href="https://msdn.microsoft.com/25cd0876-90b6-4fa3-b180-ffa0c3b51497">OleRegEnumVerbs</a>, provide a way for developers of custom DLL object applications to emulate the behavior of OLE's default object handler in getting information about objects from the registry. By using these functions, you avoid the considerable work of writing your own, and the pitfalls inherent in working directly in the registry. In addition, you get future enhancements and optimizations of these functions without having to code them yourself.





## -see-also




<a href="https://msdn.microsoft.com/8ffffa01-d118-4955-84d1-a4659ba9ddc9">IOleObject::GetUserType</a>



<a href="https://msdn.microsoft.com/6caebc68-a136-40f2-92d8-7f8003c18e5c">OleRegEnumFormatEtc</a>



<a href="https://msdn.microsoft.com/25cd0876-90b6-4fa3-b180-ffa0c3b51497">OleRegEnumVerbs</a>



<a href="https://msdn.microsoft.com/3166955f-4f7a-4904-a7fb-ebdfb8e56baf">OleRegGetMiscStatus</a>
 

 


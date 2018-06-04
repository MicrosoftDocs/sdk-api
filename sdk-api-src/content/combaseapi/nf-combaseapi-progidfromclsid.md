---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ProgIDFromCLSID function


## -description


Retrieves the ProgID for a given CLSID.




## -parameters




### -param clsid [in]

The CLSID for which the ProgID is to be requested.


### -param lplpszProgID [out]

The address of a pointer variable that receives the ProgID string. The string that represents <i>clsid</i> includes enclosing braces.


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
The ProgID was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
Class not registered in the registry.

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
</table>
 




## -remarks



Every OLE object class listed in the <b>Insert Object</b> dialog box must have a programmatic identifier (ProgID), a string that uniquely identifies a given class, stored in the registry. In addition to determining the eligibility for the <b>Insert Object</b> dialog box, the ProgID can be used as an identifier in a macro programming language to identify a class. Finally, the ProgID is also the class name used for an object of an OLE class that is placed in an OLE 1 container.

<b>ProgIDFromCLSID</b> uses entries in the registry to do the conversion. OLE application authors are responsible for ensuring that the registry is configured correctly in the application's setup program.

The ProgID string must be different than the class name of any OLE 1 application, including the OLE 1 version of the same application, if there is one. In addition, a ProgID string must not contain more than 39 characters, start with a digit, or, except for a single period, contain any punctuation (including underscores).

The ProgID must never be shown to the user in the user interface. If you need a short displayable string for an object, call <a href="https://msdn.microsoft.com/492a4084-494e-4d78-8f3a-853ec486a2d6">IOleObject::GetUserType</a>.



Call the <a href="https://msdn.microsoft.com/89fb20af-65bf-4ed4-9f71-eb707ee8eb09">CLSIDFromProgID</a> function to find the CLSID associated with a given ProgID. Be sure to free the returned ProgID  when you are finished with it by calling the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.




## -see-also




<a href="https://msdn.microsoft.com/89fb20af-65bf-4ed4-9f71-eb707ee8eb09">CLSIDFromProgID</a>
 

 


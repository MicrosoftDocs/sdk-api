---
UID: NF:combaseapi.ProgIDFromCLSID
title: ProgIDFromCLSID function (combaseapi.h)
description: Retrieves the ProgID for a given CLSID.
helpviewer_keywords: ["ProgIDFromCLSID","ProgIDFromCLSID function [COM]","_com_ProgIDFromCLSID","com.progidfromclsid","combaseapi/ProgIDFromCLSID"]
old-location: com\progidfromclsid.htm
tech.root: com
ms.assetid: a863cbc2-f8ab-468a-8254-b273077a6a2b
ms.date: 12/05/2018
ms.keywords: ProgIDFromCLSID, ProgIDFromCLSID function [COM], _com_ProgIDFromCLSID, com.progidfromclsid, combaseapi/ProgIDFromCLSID
req.header: combaseapi.h
req.include-header: Objbase.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ProgIDFromCLSID
 - combaseapi/ProgIDFromCLSID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - ProgIDFromCLSID
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

The ProgID must never be shown to the user in the user interface. If you need a short displayable string for an object, call <a href="/windows/desktop/api/ole2/nf-ole2-olereggetusertype">IOleObject::GetUserType</a>.



Call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid">CLSIDFromProgID</a> function to find the CLSID associated with a given ProgID. Be sure to free the returned ProgID  when you are finished with it by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid">CLSIDFromProgID</a>
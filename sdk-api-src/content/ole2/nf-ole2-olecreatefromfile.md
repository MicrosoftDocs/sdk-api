---
UID: NF:ole2.OleCreateFromFile
title: OleCreateFromFile function (ole2.h)
description: Creates an embedded object from the contents of a named file.
helpviewer_keywords: ["OleCreateFromFile","OleCreateFromFile function [COM]","_ole_OleCreateFromFile","com.olecreatefromfile","ole/OleCreateFromFile"]
old-location: com\olecreatefromfile.htm
tech.root: com
ms.assetid: 98c63646-6617-46b6-8c3e-82d1c4d0adb6
ms.date: 12/05/2018
ms.keywords: OleCreateFromFile, OleCreateFromFile function [COM], _ole_OleCreateFromFile, com.olecreatefromfile, ole/OleCreateFromFile
f1_keywords:
- ole2/OleCreateFromFile
dev_langs:
- c++
req.header: ole2.h
req.include-header: Ole2.h
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
api_name:
- OleCreateFromFile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OleCreateFromFile function


## -description


Creates an embedded object from the contents of a named file.




## -parameters




#### - rclsid [in]

This parameter is reserved and must be CLSID_NULL.


#### - lpszFileName [in]

Pointer to a string specifying the full path of the file from which the object should be initialized.


#### - riid [in]

Reference to the identifier of the interface the caller later uses to communicate with the new object (usually IID_IOleObject, defined in the OLE headers as the interface ID of <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>).


#### - renderopt [in]

Value from the enumeration <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. The <b>OLERENDER</b> value chosen affects the possible values for the <i>lpFormatEtc</i> parameter.


#### - lpFormatEtc [in]

 Depending on which of the <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a> flags is used as the value of <i>renderopt</i>, pointer to one of the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> enumeration values. Refer also to the <b>OLERENDER</b> enumeration for restrictions.


#### - pClientSite [in]

Pointer to an instance of <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>, the primary interface through which the object will request services from its container. This parameter can be <b>NULL</b>.


#### - pStg [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface on the storage object. This parameter cannot be <b>NULL</b>.


#### - ppvObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly created object.


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
<dt><b>STG_E_FILENOTFOUND </b></dt>
</dl>
</td>
<td width="60%">
File not bound.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_CANT_BINDTOSOURCE</b></dt>
</dl>
</td>
<td width="60%">
Not able to bind to source.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_MEDIUMFULL</b></dt>
</dl>
</td>
<td width="60%">
The medium is full.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_TYMED</b></dt>
</dl>
</td>
<td width="60%">
Invalid <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ne-objidl-tymed">TYMED</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_LINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid LINDEX.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_FORMATETC</b></dt>
</dl>
</td>
<td width="60%">
Invalid <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure.

</td>
</tr>
</table>
 




## -remarks



The <b>OleCreateFromFile</b> function creates a new embedded object from the contents of a named file. If the ProgID in the registration database contains the PackageOnFileDrop key, it creates a package. If not, the function calls the <a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-getclassfile">GetClassFile</a> function to get the CLSID associated with the <i>lpszFileName</i> parameter, and then creates an OLE 2-embedded object associated with that CLSID. The <i>rclsid</i> parameter of <b>OleCreateFromFile</b> will always be ignored, and should be set to CLSID_NULL.

As for other OleCreateXxx functions, the newly created object is not shown to the user for editing, which requires a <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-doverb">DoVerb</a> operation. It is used to implement insert file operations.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-getclassfile">GetClassFile</a>
 

 


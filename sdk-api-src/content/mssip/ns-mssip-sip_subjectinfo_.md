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

# SIP_SUBJECTINFO_ structure


## -description


The <b>SIP_SUBJECTINFO</b> structure specifies subject information data to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface package</a> (SIP) APIs.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field pgSubjectType

A pointer to a <b>GUID</b> structure that identifies the subject type.


### -field hFile

A file handle that represents the subject. If the storage type of the subject is a file, set <i>hFile</i> to <b>INVALID_HANDLE_VALUE</b> and set the <i>pwsFileName</i> parameter to the name of the file.


### -field pwsFileName

A pointer to a null-terminated Unicode string that contains the file name of the subject.


### -field pwsDisplayName

A pointer to a null-terminated Unicode string that contains the display name of 
                                                the subject.


### -field dwReserved1

This member is reserved for future use.


### -field dwIntVersion

This member is reserved. Do not modify  this member. It is used by the SIP to pass the internal version number
                                                between get and verify functions.


### -field hProv

An <a href="https://msdn.microsoft.com/8ec6b392-06bc-4717-8657-7ea9a43d03fb">HCRYPTPROV</a> handle to the cryptography provider.


### -field DigestAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the identifier for the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> algorithm used to hash the file.


### -field dwFlags

A value that modifies the behavior of the functions that use this structure. For more information about possible values for this member, see the <i>dwFlags</i> parameter of <a href="https://msdn.microsoft.com/9921ffae-2299-4bf2-b76d-77f7f6afb663">SignerSignEx</a>.


### -field dwEncodingType

A value that specifies the encoding type used for the file. Currently, only <b>X509_ASN_ENCODING</b> and <b>PKCS_7_ASN_ENCODING</b> are being used; however, additional encoding types may be added in the future. For either current encoding type, use: <b>X509_ASN_ENCODING</b> | <b>PKCS_7_ASN_ENCODING</b>.


### -field dwReserved2

This member is reserved  for future use.


### -field fdwCAPISettings

This member is not used.


### -field fdwSecuritySettings

This member is not used.


### -field dwIndex

The message index of the last call to <b>CryptSIPGetSignedDataMsg</b>. operation.


### -field dwUnionChoice

Specifies the type of additional information provided.

<table>
<tr>
<th>Defined constant/value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSSIP_ADDINFO_NONE"></a><a id="mssip_addinfo_none"></a><dl>
<dt><b>MSSIP_ADDINFO_NONE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
There is no additional information about the subject.

</td>
</tr>
<tr>
<td width="40%"><a id="MSSIP_ADDINFO_FLAT"></a><a id="mssip_addinfo_flat"></a><dl>
<dt><b>MSSIP_ADDINFO_FLAT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The additional information is a flat file.

</td>
</tr>
<tr>
<td width="40%"><a id="MSSIP_ADDINFO_CATMEMBER"></a><a id="mssip_addinfo_catmember"></a><dl>
<dt><b>MSSIP_ADDINFO_CATMEMBER</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The additional information is a catalog member.

</td>
</tr>
<tr>
<td width="40%"><a id="MSSIP_ADDINFO_BLOB"></a><a id="mssip_addinfo_blob"></a><dl>
<dt><b>MSSIP_ADDINFO_BLOB</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The additional information is a <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="MSSIP_ADDINFO_NONMSSIP"></a><a id="mssip_addinfo_nonmssip"></a><dl>
<dt><b>MSSIP_ADDINFO_NONMSSIP</b></dt>
<dt>500</dt>
</dl>
</td>
<td width="60%">
The additional information is in a user defined format.

</td>
</tr>
</table>
 


### -field psFlat

An <a href="https://msdn.microsoft.com/9f5bebd1-8eda-456d-9339-3334a19c0ea4">MS_ADDINFO_FLAT</a> structure that contains additional information for flat file subject types.


### -field psCatMember

An <a href="https://msdn.microsoft.com/40a00c8a-95e4-406c-b04e-0d29beb70d67">MS_ADDINFO_CATALOGMEMBER</a> structure that contains additional information for catalog member subject types.


### -field psBlob

An <a href="https://msdn.microsoft.com/236c8778-0b80-4157-8a81-24712ebf9a77">MS_ADDINFO_BLOB</a> structure that contains additional information for BLOB subject types.


### -field pClientData

A pointer to SIP-specific data.


## -remarks



Upon first use of the <b>SIP_SUBJECTINFO</b> structure, initialize the entire structure to binary zero. Do not initialize the structure between SIP function calls.

Subjects include, but are not limited to, portable executable images (.exe), cabinet (.cab) images, flat files, and catalog files. Each subject type uses a different subset of its data for hash calculation and requires a different procedure for storage and retrieval. Therefore each subject type has a unique subject interface package specification.




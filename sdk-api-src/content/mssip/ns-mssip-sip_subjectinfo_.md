---
UID: NS:mssip.SIP_SUBJECTINFO_
title: SIP_SUBJECTINFO_
author: windows-driver-content
description: Specifies subject information data to the subject interface package (SIP) APIs.
old-location: security\sip_subjectinfo.htm
old-project: SecCrypto
ms.assetid: 6274cd08-d67f-410d-9303-3a42b7f1edc6
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*LPSIP_SUBJECTINFO, LPSIP_SUBJECTINFO, LPSIP_SUBJECTINFO structure pointer [Security], MSSIP_ADDINFO_BLOB, MSSIP_ADDINFO_CATMEMBER, MSSIP_ADDINFO_FLAT, MSSIP_ADDINFO_NONE, MSSIP_ADDINFO_NONMSSIP, SIP_SUBJECTINFO, SIP_SUBJECTINFO structure [Security], SIP_SUBJECTINFO_, mssip/LPSIP_SUBJECTINFO, mssip/SIP_SUBJECTINFO, security.sip_subjectinfo"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mssip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SIP_SUBJECTINFO, *LPSIP_SUBJECTINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mssip.h
api_name:
-	SIP_SUBJECTINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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




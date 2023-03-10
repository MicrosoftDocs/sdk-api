---
UID: NS:mscat.CRYPTCATMEMBER_
title: CRYPTCATMEMBER (mscat.h)
description: The CRYPTCATMEMBER structure provides information about a catalog member. This structure is used by the CryptCATGetMemberInfo and CryptCATEnumerateAttr functions.
helpviewer_keywords: ["CRYPTCATMEMBER","CRYPTCATMEMBER structure [Security]","mscat/CRYPTCATMEMBER","security.cryptcatmember"]
old-location: security\cryptcatmember.htm
tech.root: security
ms.assetid: 08f663d9-9dc2-4ac9-95c5-7f2ed972eb9b
ms.date: 12/05/2018
ms.keywords: CRYPTCATMEMBER, CRYPTCATMEMBER structure [Security], mscat/CRYPTCATMEMBER, security.cryptcatmember
req.header: mscat.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CRYPTCATMEMBER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CRYPTCATMEMBER_
 - mscat/CRYPTCATMEMBER_
 - CRYPTCATMEMBER
 - mscat/CRYPTCATMEMBER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mscat.h
api_name:
 - CRYPTCATMEMBER
---

# CRYPTCATMEMBER structure


## -description

<p class="CCE_Message">[The  <b>CRYPTCATMEMBER</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTCATMEMBER</b> structure provides information about a catalog member. This structure is used by the <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatgetmemberinfo">CryptCATGetMemberInfo</a> and <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatenumerateattr">CryptCATEnumerateAttr</a> functions.

## -struct-fields

### -field cbStruct

The size, in bytes, of this structure.

### -field pwszReferenceTag

A pointer to a null-terminated string that contains the reference tag value.

### -field pwszFileName

A pointer to a null-terminated string that contains the file name.

### -field gSubjectType

<b>GUID</b> that identifies the subject type.

### -field fdwMemberFlags

Value that specifies the member flags.

### -field pIndirectData

A pointer to a <b>SIP_INDIRECT_DATA</b> structure.

### -field dwCertVersion

Value that specifies the certificate version.

### -field dwReserved

Reserved; do not use.

### -field hReserved

Reserved; do not use.

### -field sEncodedIndirectData

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_ATTR_BLOB</a> structure that contains encoded indirect data.

### -field sEncodedMemberInfo

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_ATTR_BLOB</a> structure that contains encoded member information.

## -see-also

<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatenumerateattr">CryptCATEnumerateAttr</a>



<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatgetmemberinfo">CryptCATGetMemberInfo</a>
---
UID: NF:dsparse.DsGetRdnW
title: DsGetRdnW function (dsparse.h)
description: Retrieves the key and value of the first relative distinguished name and a pointer to the next relative distinguished name from a distinguished name string.
helpviewer_keywords: ["DsGetRdnW","DsGetRdnW function [Active Directory]","ad.dsgetrdnw","dsparse/DsGetRdnW"]
old-location: ad\dsgetrdnw.htm
tech.root: ad
ms.assetid: 22627f2e-adfb-49de-bae5-20aaf69830ac
ms.date: 12/05/2018
ms.keywords: DsGetRdnW, DsGetRdnW function [Active Directory], ad.dsgetrdnw, dsparse/DsGetRdnW
req.header: dsparse.h
req.include-header: Ntdsapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsGetRdnW
 - dsparse/DsGetRdnW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsGetRdnW
---

# DsGetRdnW function


## -description

The <b>DsGetRdnW</b> function retrieves the key and value of the first relative distinguished name and a pointer to the next relative distinguished name from a distinguished name string.

## -parameters

### -param ppDN [in, out]

Address of a Unicode string pointer that, on entry, contains the distinguished name string to be parsed. The length of this string is specified in the <i>pcDN</i> parameter. If the function succeeds, this parameter is adjusted to point to the remainder of the distinguished name exclusive of current relative distinguished name. For example, if this parameter points to the string "dc=corp,dc=fabrikam,dc=com", after the function is complete this parameter points to the string ",dc=fabrikam,dc=com".

### -param pcDN [in, out]

Pointer to a <b>DWORD</b> value that, on entry, contains the number of characters in the <i>ppDN</i> string. If the function succeeds, this parameter receives the number of characters in the remainder of the distinguished name. These values do not include the null-terminated character.

### -param ppKey [out]

Pointer to a <b>LPCWCH</b> value that, if the function succeeds, receives a pointer to the key in the relative distinguished name string. This pointer is within the <i>ppDN</i> string and is not null-terminated. The <i>pcKey</i> parameter receives the number of characters in the key. This parameter is undefined if <i>pcKey</i> receives zero.

### -param pcKey [out]

Pointer to a <b>DWORD</b> value that, if the function succeeds, receives the number of characters in the key string represented by the <i>ppKey</i> parameter. If this parameter receives zero, <i>ppKey</i> is undefined.

### -param ppVal [out]

Pointer to a <b>LPCWCH</b> value that, if the function is successful, receives a pointer to the value in the relative distinguished name string. This pointer is within the <i>ppDN</i> string and is not null-terminated. The <i>pcVal</i> parameter receives the number of characters in the value. This parameter is undefined if <i>pcVal</i> receives zero.

### -param pcVal [out]

Pointer to a <b>DWORD</b> value that, if the function succeeds, receives the number of characters in the value string represented by the <i>ppVal</i> parameter. If this parameter receives zero, <i>ppVal</i> is undefined.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Win32 error code otherwise. Possible error codes include the following values.

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>
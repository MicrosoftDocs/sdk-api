---
UID: NF:dsparse.DsCrackSpnA
title: DsCrackSpnA function (dsparse.h)
description: Parses a service principal name (SPN) into its component strings. (ANSI)
helpviewer_keywords: ["DsCrackSpnA", "dsparse/DsCrackSpnA"]
old-location: ad\dscrackspn.htm
tech.root: ad
ms.assetid: 65c81c23-a259-480c-9c1e-03484d3e89c9
ms.date: 12/05/2018
ms.keywords: DsCrackSpn, DsCrackSpn function [Active Directory], DsCrackSpnA, DsCrackSpnW, _glines_dscrackspn, ad.dscrackspn, dsparse/DsCrackSpn, dsparse/DsCrackSpnA, dsparse/DsCrackSpnW
req.header: dsparse.h
req.include-header: Ntdsapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsCrackSpnW (Unicode) and DsCrackSpnA (ANSI)
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
 - DsCrackSpnA
 - dsparse/DsCrackSpnA
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
 - DsCrackSpn
 - DsCrackSpnA
 - DsCrackSpnW
---

# DsCrackSpnA function


## -description

The <b>DsCrackSpn</b> function parses a service principal name (SPN) into its component strings.

## -parameters

### -param pszSpn [in]

Pointer to a constant null-terminated string that contains the SPN to parse. The SPN has the following format, in which the &lt;service class&gt; and &lt;instance name&gt; components must be present and the &lt;port number&gt; and &lt;service name&gt; components are optional. The &lt;port number&gt; component must be a numeric string value.


```cpp
<service class>/<instance name>:<port number>/<service name>
```

### -param pcServiceClass [in, out, optional]

Pointer to a <b>DWORD</b> value that, on entry, contains the size, in <b>TCHARs</b>, of the <i>ServiceClass</i> buffer, including the terminating null character. On exit, this parameter contains the number of <b>TCHARs</b> in the <i>ServiceClass</i> string, including the terminating null character.

If this parameter is <b>NULL</b>, contains zero, or <i>ServiceClass</i> is <b>NULL</b>, this parameter and  <i>ServiceClass</i> are ignored.

To obtain the number of characters required for the <i>ServiceClass</i> string, including the null terminator, call this function with a valid SPN, a non-<b>NULL</b> <i>ServiceClass</i> and this parameter set to 1.

### -param ServiceClass [out, optional]

Pointer to a <b>TCHAR</b> buffer that receives a null-terminated string containing the &lt;service class&gt; component of the SPN. This buffer must be at least <i>*pcServiceClass </i><b>TCHARs</b> in size. This parameter may be  <b>NULL</b> if the service class is not required.

### -param pcServiceName [in, out, optional]

Pointer to a <b>DWORD</b> value that, on entry, contains the size, in <b>TCHARs</b>, of the <i>ServiceName</i> buffer, including the terminating null character. On exit, this parameter contains the number of <b>TCHARs</b> in the <i>ServiceName</i> string, including the terminating null character.

If this parameter is <b>NULL</b>, contains zero, or <i>ServiceName</i> is <b>NULL</b>, this parameter and  <i>ServiceName</i> are ignored.

To obtain the number of characters required for the <i>ServiceName</i> string, including the null terminator, call this function with a valid SPN, a non-<b>NULL</b> <i>ServiceName</i> and this parameter set to 1.

### -param ServiceName [out, optional]

Pointer to a <b>TCHAR</b> buffer that receives a null-terminated string containing the &lt;service name&gt; component of the SPN. This buffer must be at least <i>*pcServiceName </i><b>TCHARs</b> in size. If the &lt;service name&gt; component is not present in the SPN, this buffer  receives the &lt;instance name&gt; component. This parameter may be <b>NULL</b> if the service name is not required.

### -param pcInstanceName [in, out, optional]

Pointer to a <b>DWORD</b> value that, on entry, contains the size, in <b>TCHARs</b>, of the <i>InstanceName</i> buffer, including the terminating null character. On exit, this parameter contains the number of <b>TCHARs</b> in the <i>InstanceName</i> string, including the terminating null character.

If this parameter is <b>NULL</b>, contains zero, or <i>InstanceName</i> is <b>NULL</b>, this parameter and <i>InstanceName</i> are ignored.

To obtain the number of characters required for the <i>InstanceName</i> string, including the null terminator, call this function with a valid SPN, a non-<b>NULL</b> <i>InstanceName</i> and this parameter set to 1.

### -param InstanceName [out, optional]

Pointer to a <b>TCHAR</b> buffer that receives a null-terminated string containing the &lt;instance name&gt; component of the SPN. This buffer must be at least <i>*pcInstanceName </i> <b>TCHARs</b> in size. This parameter may be  <b>NULL</b> if the instance name is not required.

### -param pInstancePort [out, optional]

Pointer to a <b>DWORD</b> value that receives the integer value of the &lt;port number&gt; component of the SPN. If the SPN does not contain a &lt;port number&gt; component, this parameter receives zero. This parameter may be  <b>NULL</b> if the port number is not required.

## -returns

Returns a Win32 error code, including the following.

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>

## -remarks

> [!NOTE]
> The dsparse.h header defines DsCrackSpn as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

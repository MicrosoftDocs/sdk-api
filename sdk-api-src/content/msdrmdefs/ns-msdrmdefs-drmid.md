---
UID: NS:msdrmdefs._DRMID
title: DRMID (msdrmdefs.h)
description: Identifies an object.
helpviewer_keywords: ["DRMID","DRMID structure [Active Directory Rights Management Services SDK 1.0]","msdrmdefs/DRMID","rm.drmid"]
old-location: rm\drmid.htm
tech.root: rm
ms.assetid: 8b7f22e0-586e-4950-94fe-868b3fc91ffa
ms.date: 12/05/2018
ms.keywords: DRMID, DRMID structure [Active Directory Rights Management Services SDK 1.0], msdrmdefs/DRMID, rm.drmid
req.header: msdrmdefs.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DRMID
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - _DRMID
 - msdrmdefs/_DRMID
 - DRMID
 - msdrmdefs/DRMID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msdrmdefs.h
api_name:
 - DRMID
---

# DRMID structure


## -description

>[!Note]
>[The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, which leverages functionality exposed by the client in Msipc.dll.

The <b>DRMID</b> structure identifies an object. It is used by the <a href="/windows/desktop/api/msdrmdefs/ns-msdrmdefs-drmboundlicenseparams">DRMBOUNDLICENSEPARAMS</a> structure and by the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateenablingprincipal">DRMCreateEnablingPrincipal</a> function.

## -struct-fields

### -field uVersion

Specifies the version of the structure. If you are programming in C, this should be set to <b>DRMIDVERSION</b> (0).

### -field wszIDType

A pointer to a null-terminated Unicode string that contains the ID type. If you are using this parameter to create a bound license, you must specify the same value that you set in the <i>wszIDType</i> parameter of the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetmetadata">DRMSetMetaData</a> function. For more information, see <a href="/windows/desktop/api/msdrmdefs/ns-msdrmdefs-drmboundlicenseparams">DRMBOUNDLICENSEPARAMS</a>. If you are using this parameter in  the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateenablingprincipal">DRMCreateEnablingPrincipal</a> function, the value can be <b>NULL</b>.

### -field wszID

A pointer to a null-terminated Unicode string that contains the object ID. If you are using this parameter to create a bound license, you must specify the same value that you set in the <i>wszID</i> parameter of the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmsetmetadata">DRMSetMetaData</a> function. For more information, see <a href="/windows/desktop/api/msdrmdefs/ns-msdrmdefs-drmboundlicenseparams">DRMBOUNDLICENSEPARAMS</a>. If you are using this parameter in  the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateenablingprincipal">DRMCreateEnablingPrincipal</a> function, the value can be <b>NULL</b>.

### -field _DRMID

TBD

## -remarks

In a C++ application, this structure will have a default constructor that initializes the members to the following values.


```cpp
uVersion = DRMIDVERSION
wszIDType = NULL
wszID = NULL

```


An overloaded C++ constructor is also defined as follows.


```cpp
DRMID(PWSTR wszIDType, PWSTR wszID)
```


 This constructor will initialize the members to the following values.


```cpp
uVersion = DRMIDVERSION
wszIDType = wszTypein
wszID = wszIDin

```

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-structures">AD RMS Structures</a>



<a href="/windows/desktop/api/msdrmdefs/ns-msdrmdefs-drmboundlicenseparams">DRMBOUNDLICENSEPARAMS</a>
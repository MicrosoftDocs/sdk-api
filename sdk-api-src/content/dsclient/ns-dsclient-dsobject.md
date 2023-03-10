---
UID: NS:dsclient.DSOBJECT
title: DSOBJECT (dsclient.h)
description: Contains directory object data.
helpviewer_keywords: ["*LPDSOBJECT","DSOBJECT","DSOBJECT structure [Active Directory]","DSOBJECT_ISCONTAINER","DSOBJECT_READONLYPAGES","DSPROVIDER_ADVANCED","DSPROVIDER_UNUSED_0","DSPROVIDER_UNUSED_1","DSPROVIDER_UNUSED_2","DSPROVIDER_UNUSED_3","LPDSOBJECT","LPDSOBJECT structure pointer [Active Directory]","_glines_dsobject","ad.dsobject","dsclient/DSOBJECT","dsclient/LPDSOBJECT"]
old-location: ad\dsobject.htm
tech.root: ad
ms.assetid: 2f16a015-a777-4410-bed5-d409a4869c97
ms.date: 12/05/2018
ms.keywords: '*LPDSOBJECT, DSOBJECT, DSOBJECT structure [Active Directory], DSOBJECT_ISCONTAINER, DSOBJECT_READONLYPAGES, DSPROVIDER_ADVANCED, DSPROVIDER_UNUSED_0, DSPROVIDER_UNUSED_1, DSPROVIDER_UNUSED_2, DSPROVIDER_UNUSED_3, LPDSOBJECT, LPDSOBJECT structure pointer [Active Directory], _glines_dsobject, ad.dsobject, dsclient/DSOBJECT, dsclient/LPDSOBJECT'
req.header: dsclient.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DSOBJECT, *LPDSOBJECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPDSOBJECT
 - dsclient/LPDSOBJECT
 - DSOBJECT
 - dsclient/DSOBJECT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsclient.h
api_name:
 - DSOBJECT
---

# DSOBJECT structure


## -description

The <b>DSOBJECT</b> structure contains directory object data. An array of this structure is provided in the <b>aObjects</b> member of the <a href="/windows/desktop/api/dsclient/ns-dsclient-dsobjectnames">DSOBJECTNAMES</a> structure.

## -struct-fields

### -field dwFlags

Contains a set of flags that provide object data. This can be zero or a combination of one, or more, of the following values.



#### DSOBJECT_ISCONTAINER

The object is a container.



#### DSOBJECT_READONLYPAGES

When displaying properties for this object, the user interface must be read-only.

### -field dwProviderFlags

Contains a set of flags that provide data about the object provider. This can be zero or a combination of one or more of the following values.



#### DSPROVIDER_ADVANCED

The user interface for this object should be shown in an advanced mode.



#### DSPROVIDER_UNUSED_0

Not used.



#### DSPROVIDER_UNUSED_1

Not used.



#### DSPROVIDER_UNUSED_2

Not used.



#### DSPROVIDER_UNUSED_3

Not used.

### -field offsetName

Contains the offset, in bytes, from the start of the <a href="/windows/desktop/api/dsclient/ns-dsclient-dsobjectnames">DSOBJECTNAMES</a> structure to a NULL-terminated, Unicode string that contains the ADSPath of the object.

The following code example shows how to use this member.


```cpp
pwszName = (LPWSTR)((LPBYTE)pdsObjNames + 
    pdsObjNames->aObjects[i].offsetName);

```

### -field offsetClass

Contains the offset, in bytes, from the start of the <a href="/windows/desktop/api/dsclient/ns-dsclient-dsobjectnames">DSOBJECTNAMES</a> structure to a NULL-terminated, Unicode string that contains the class name of the object. Contains zero if the class name is unknown.

The following code example shows how to use this member.


```cpp
pwszClass = (LPWSTR)((LPBYTE)pdsObjNames + 
    pdsObjNames->aObjects[i].offsetClass);

```

## -see-also

<a href="/windows/desktop/api/dsclient/ns-dsclient-dsobjectnames">DSOBJECTNAMES</a>



<a href="/windows/desktop/AD/display-structures-in-active-directory-domain-services">Display Structures in Active Directory Domain Services</a>


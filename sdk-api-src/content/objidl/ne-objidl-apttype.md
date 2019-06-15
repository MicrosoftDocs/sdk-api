---
UID: NE:objidl._APTTYPE
title: APTTYPE (objidl.h)
author: windows-sdk-content
description: Specifies different types of apartments.
old-location: com\apttype.htm
tech.root: com
ms.assetid: eae95b1f-3883-4334-aa7e-84e71e05fb24
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: APTTYPE, APTTYPE enumeration [COM], APTTYPE_CURRENT, APTTYPE_MAINSTA, APTTYPE_MTA, APTTYPE_NA, APTTYPE_STA, _com_APTTYPE, com.apttype, objidlbase/APTTYPE, objidlbase/APTTYPE_CURRENT, objidlbase/APTTYPE_MAINSTA, objidlbase/APTTYPE_MTA, objidlbase/APTTYPE_NA, objidlbase/APTTYPE_STA
ms.topic: enum
req.header: objidl.h
req.include-header: Objidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - APTTYPE
product: Windows
targetos: Windows
req.typenames: APTTYPE
req.redist: 
ms.custom: 19H1
---

# APTTYPE enumeration


## -description


Specifies different types of apartments.


## -enum-fields




### -field APTTYPE_CURRENT

The current thread.


### -field APTTYPE_STA

A single-threaded apartment.


### -field APTTYPE_MTA

A multithreaded apartment.


### -field APTTYPE_NA

A neutral apartment.


### -field APTTYPE_MAINSTA

The main single-threaded apartment.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetapartmenttype">CoGetApartmentType</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-icomthreadinginfo-getcurrentapartmenttype">IComThreadingInfo::GetCurrentApartmentType</a>
 

 


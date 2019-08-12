---
UID: NS:objidl.tagSOLE_AUTHENTICATION_LIST
title: SOLE_AUTHENTICATION_LIST (objidl.h)
author: windows-sdk-content
description: Indicates the default authentication information to use with each authentication service.
old-location: com\sole_authentication_list.htm
tech.root: com
ms.assetid: 21f7aef3-b6be-41cc-a6ed-16d3778e3cee
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSOLE_AUTHENTICATION_LIST, PSOLE_AUTHENTICATION_LIST, PSOLE_AUTHENTICATION_LIST structure pointer [COM], SOLE_AUTHENTICATION_LIST, SOLE_AUTHENTICATION_LIST structure [COM], _com_SOLE_AUTHENTICATION_LIST, com.sole_authentication_list, objidlbase/PSOLE_AUTHENTICATION_LIST, objidlbase/SOLE_AUTHENTICATION_LIST, tagSOLE_AUTHENTICATION_LIST"
ms.topic: struct
f1_keywords: 
 - "objidl/SOLE_AUTHENTICATION_LIST"
req.header: objidl.h
req.include-header: Objidl.h
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
 - SOLE_AUTHENTICATION_LIST
product: Windows
targetos: Windows
req.typenames: SOLE_AUTHENTICATION_LIST, *PSOLE_AUTHENTICATION_LIST
req.redist: 
ms.custom: 19H1
---

# SOLE_AUTHENTICATION_LIST structure


## -description


Indicates the default authentication information to use with each authentication service. When DCOM negotiates the default authentication service for a proxy, it picks the default authentication information from this list.



## -struct-fields




### -field cAuthInfo

The count of pointers in the array pointed to by <b>aAuthInfo</b>. 


### -field aAuthInfo

An array of <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-sole_authentication_info">SOLE_AUTHENTICATION_INFO</a> structures. Each of these structures contains an identifier for an authentication service, an identifier for the authorization service, and a pointer to authentication information to use with the specified authentication service.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>
 

 


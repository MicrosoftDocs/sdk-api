---
UID: NS:searchapi._AUTHENTICATION_INFO
title: "_AUTHENTICATION_INFO"
author: windows-sdk-content
description: Describes security authentication information for content access.
old-location: search\_search_AUTHENTICATION_INFO.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\authentication_info.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: AUTHENTICATION_INFO, AUTHENTICATION_INFO structure [search], _AUTHENTICATION_INFO, _search_AUTHENTICATION_INFO, search._search_AUTHENTICATION_INFO, searchapi/AUTHENTICATION_INFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Srchprth.idl
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
 - Searchapi.h
api_name:
 - AUTHENTICATION_INFO
product: Windows
targetos: Windows
req.typenames: AUTHENTICATION_INFO
req.redist: Windows Desktop Search (WDS) 3.0
---

# _AUTHENTICATION_INFO structure


## -description


Describes security authentication information for content access.


## -struct-fields




### -field dwSize

Type: <b>DWORD</b>

Size of the structure, in bytes.
                


### -field atAuthenticationType

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa965687(v=VS.85).aspx">AUTH_TYPE</a></b>

Flag to describe the type of authentication. For a list of possible values, see the <a href="https://msdn.microsoft.com/en-us/library/Aa965687(v=VS.85).aspx">AUTH_TYPE</a> enumerated type.


### -field pcwszUser

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string containing the user name.
                


### -field pcwszPassword

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string containing the password for <b> pcwszUser</b>.
                


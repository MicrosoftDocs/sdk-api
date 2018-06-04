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

# SHObjectProperties function


## -description


<p class="CCE_Message">[<b>SHObjectProperties</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Invokes the <b>Properties</b> context menu command on a Shell object.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle of the parent window of the dialog box. This value can be <b>NULL</b>.


### -param shopObjectType [in]

Type: <b>DWORD</b>

A flag value that specifies the type of object.



#### SHOP_PRINTERNAME

<i>pszObjectName</i> contains the friendly name of a printer.



#### SHOP_FILEPATH

<i>pszObjectName</i> contains a fully qualified file name.



#### SHOP_VOLUMEGUID

<i>pszObjectName</i> contains either (a) a volume name of the form \\?\Volume{GUID}\, where {GUID} is a globally unique identifier (for example, "\\?\Volume\{2eca078d-5cbc-43d3-aff8-7e8511f60d0e}\)", or (b) a drive path (for example, "C:\").



### -param pszObjectName [in]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the object name. The contents of the string are determined by the flag set in <i>shopObjectType</i>.


### -param pszPropertyPage [in]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the name of the property sheet page to be opened initially. Set this parameter to <b>NULL</b> to specify the default page.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if the command is successfully invoked; otherwise, <b>FALSE</b>.




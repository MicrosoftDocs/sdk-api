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

# _openasinfo structure


## -description


Stores information for the <a href="https://msdn.microsoft.com/026bfb34-a8a5-4bd7-9bc0-4aa395e6d535">SHOpenWithDialog</a> function.


## -struct-fields




### -field pcszFile

Type: <b>LPCWSTR</b>

A pointer to the file name.


### -field pcszClass

Type: <b>LPCWSTR</b>

A pointer to the file type description. Set this parameter to <b>NULL</b> to use the file name extension of <b>pcszFile</b>.


### -field oaifInFlags

Type: <b>OPEN_AS_INFO_FLAGS</b>

The characteristics of the <a href="https://msdn.microsoft.com/026bfb34-a8a5-4bd7-9bc0-4aa395e6d535">SHOpenWithDialog</a> dialog box. One or more of the following values.



#### OAIF_ALLOW_REGISTRATION (0x00000001)

Enable the "always use this program" checkbox. If not passed, it will be disabled.



#### OAIF_REGISTER_EXT (0x00000002)

Do the registration after the user hits the <b>OK</b> button.



#### OAIF_EXEC (0x00000004)

Execute file after registering.



#### OAIF_FORCE_REGISTRATION (0x00000008)

Force the <b>Always use this program</b> checkbox to be checked. Typically, you won't use the OAIF_ALLOW_REGISTRATION flag when you pass this value.



#### OAIF_HIDE_REGISTRATION (0x00000020)

<b>Introduced in Windows Vista</b>. Hide the <b>Always use this program</b> checkbox. If this flag is specified, the OAIF_ALLOW_REGISTRATION and OAIF_FORCE_REGISTRATION flags will be ignored.



#### OAIF_URL_PROTOCOL (0x00000040)

<b>Introduced in Windows Vista</b>. The value for the extension that is passed is actually a protocol, so the <b>Open With</b> dialog box should show applications that are registered as capable of handling that protocol.



#### OAIF_FILE_IS_URI (0x00000080)

<b>Introduced in Windows 8</b>. The location pointed to by the <i>pcszFile</i> parameter is given as a URI.


## -remarks



Starting in Windows 10, the <b>OAIF_ALLOW_REGISTRATION</b>, <b>OAIF_FORCE_REGISTRATION</b>, and <b>OAIF_HIDE_REGISTRATION</b> flags will be ignored by <a href="https://msdn.microsoft.com/026bfb34-a8a5-4bd7-9bc0-4aa395e6d535">SHOpenWithDialog</a>. The <b>Open With</b> dialog box can no longer be used to change the default program used to open a file extension. You can only use <b>SHOpenWithDialog</b> to open a single file.




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

# _tagSOFTDISTINFO structure


## -description


Contains information about a software update.


## -struct-fields




### -field cbSize

Type: <b>ULONG</b>

The size of the structure, in bytes.


### -field dwFlags

Type: <b>DWORD</b>

This parameter can take one of the following values.



#### SOFTDIST_FLAG_USAGE_EMAIL



#### SOFTDIST_FLAG_USAGE_PRECACHE



#### SOFTDIST_FLAG_USAGE_AUTOINSTALL



#### SOFTDIST_FLAG_DELETE_SUBSCRIPTION


### -field dwAdState

Type: <b>DWORD</b>

The advertised state. It can take one of the following values.



#### SOFTDIST_ADSTATE_NONE (0x00000000)

"Update available" dialog box has not been presented to the user.



#### SOFTDIST_ADSTATE_AVAILABLE (0x00000001)

"Files downloaded" dialog box has not been presented to the user.



#### SOFTDIST_ADSTATE_DOWNLOADED (0x00000002)

"Program installed" dialog box has not been presented to the user.



#### SOFTDIST_ADSTATE_INSTALLED (0x00000003)

"Program installed" dialog box has been presented to the user.


### -field szTitle

Type: <b>LPWSTR</b>

A string that contains the contents of the TITLE flag from the associated .cdf file.


### -field szAbstract

Type: <b>LPWSTR</b>

A string that contains the contents of the ABSTRACT flag from the associated .cdf file.


### -field szHREF

Type: <b>LPWSTR</b>

A string that contains the URL of the webpage to advertise or install the update.


### -field dwInstalledVersionMS

Type: <b>DWORD</b>

The most-significant unsigned long integer value of the installed version number.


### -field dwInstalledVersionLS

Type: <b>DWORD</b>

The least-significant unsigned long integer value of the installed version number.


### -field dwUpdateVersionMS

Type: <b>DWORD</b>

The most-significant unsigned long integer value of the update version number.


### -field dwUpdateVersionLS

Type: <b>DWORD</b>

The least-significant unsigned long integer value of the update version number.


### -field dwAdvertisedVersionMS

Type: <b>DWORD</b>

The most-significant unsigned long integer value of the advertised version number.


### -field dwAdvertisedVersionLS

Type: <b>DWORD</b>

The least-significant unsigned long integer value of the advertised version number.


### -field dwReserved

Type: <b>DWORD</b>

Reserved. Must be set to zero.


## -remarks



The most-significant unsigned long integer of a version number contains the major and minor version numbers. The least-significant unsigned long integer of the version number contains the custom version and build numbers.




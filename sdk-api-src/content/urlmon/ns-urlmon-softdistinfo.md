---
UID: NS:urlmon._tagSOFTDISTINFO
title: SOFTDISTINFO (urlmon.h)
description: Contains information about a software update.
helpviewer_keywords: ["*LPSOFTDISTINFO","LPSOFTDISTINFO","LPSOFTDISTINFO structure pointer [Windows Shell]","SOFTDISTINFO","SOFTDISTINFO structure [Windows Shell]","SOFTDIST_ADSTATE_AVAILABLE (0x00000001)","SOFTDIST_ADSTATE_DOWNLOADED (0x00000002)","SOFTDIST_ADSTATE_INSTALLED (0x00000003)","SOFTDIST_ADSTATE_NONE (0x00000000)","SOFTDIST_FLAG_DELETE_SUBSCRIPTION","SOFTDIST_FLAG_USAGE_AUTOINSTALL","SOFTDIST_FLAG_USAGE_EMAIL","SOFTDIST_FLAG_USAGE_PRECACHE","_win32_SOFTDISTINFO","shell.SOFTDISTINFO","urlmon/LPSOFTDISTINFO","urlmon/SOFTDISTINFO"]
old-location: shell\SOFTDISTINFO.htm
tech.root: shell
ms.assetid: e113967a-e52c-41d7-961a-2c305790543e
ms.date: 12/05/2018
ms.keywords: '*LPSOFTDISTINFO, LPSOFTDISTINFO, LPSOFTDISTINFO structure pointer [Windows Shell], SOFTDISTINFO, SOFTDISTINFO structure [Windows Shell], SOFTDIST_ADSTATE_AVAILABLE (0x00000001), SOFTDIST_ADSTATE_DOWNLOADED (0x00000002), SOFTDIST_ADSTATE_INSTALLED (0x00000003), SOFTDIST_ADSTATE_NONE (0x00000000), SOFTDIST_FLAG_DELETE_SUBSCRIPTION, SOFTDIST_FLAG_USAGE_AUTOINSTALL, SOFTDIST_FLAG_USAGE_EMAIL, SOFTDIST_FLAG_USAGE_PRECACHE, _win32_SOFTDISTINFO, shell.SOFTDISTINFO, urlmon/LPSOFTDISTINFO, urlmon/SOFTDISTINFO'
req.header: urlmon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
targetos: Windows
req.typenames: SOFTDISTINFO, *LPSOFTDISTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagSOFTDISTINFO
 - urlmon/_tagSOFTDISTINFO
 - LPSOFTDISTINFO
 - urlmon/LPSOFTDISTINFO
 - SOFTDISTINFO
 - urlmon/SOFTDISTINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Urlmon.h
api_name:
 - SOFTDISTINFO
---

# SOFTDISTINFO structure


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


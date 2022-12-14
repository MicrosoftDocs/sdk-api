---
UID: NF:shobjidl.ICDBurn.GetRecorderDriveLetter
title: ICDBurn::GetRecorderDriveLetter (shobjidl.h)
description: Gets the drive letter of a CD drive that has been marked as write-enabled.
helpviewer_keywords: ["GetRecorderDriveLetter","GetRecorderDriveLetter method [Windows Shell]","GetRecorderDriveLetter method [Windows Shell]","ICDBurn interface","ICDBurn interface [Windows Shell]","GetRecorderDriveLetter method","ICDBurn.GetRecorderDriveLetter","ICDBurn::GetRecorderDriveLetter","_shell_ICDBurn_GetRecorderDriveLetter","shell.ICDBurn_GetRecorderDriveLetter","shobjidl/ICDBurn::GetRecorderDriveLetter"]
old-location: shell\ICDBurn_GetRecorderDriveLetter.htm
tech.root: shell
ms.assetid: 5ee10152-6823-49bb-836d-3e0cf6c2bb0b
ms.date: 12/05/2018
ms.keywords: GetRecorderDriveLetter, GetRecorderDriveLetter method [Windows Shell], GetRecorderDriveLetter method [Windows Shell],ICDBurn interface, ICDBurn interface [Windows Shell],GetRecorderDriveLetter method, ICDBurn.GetRecorderDriveLetter, ICDBurn::GetRecorderDriveLetter, _shell_ICDBurn_GetRecorderDriveLetter, shell.ICDBurn_GetRecorderDriveLetter, shobjidl/ICDBurn::GetRecorderDriveLetter
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICDBurn::GetRecorderDriveLetter
 - shobjidl/ICDBurn::GetRecorderDriveLetter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICDBurn.GetRecorderDriveLetter
---

# ICDBurn::GetRecorderDriveLetter


## -description

Gets the drive letter of a CD drive that has been marked as write-enabled.

## -parameters

### -param pszDrive [out]

Type: <b>LPWSTR</b>

A pointer to a string containing the drive letter, for example "F:\".

### -param cch [in]

Type: <b>UINT</b>

The size of the string, in characters, pointed to by pszDrive. This value will normally be 4. Values larger than 4 are allowed, but the extra characters will be ignored by this method. Values less than 4 will generate an E_INVALIDARG error.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The drive whose letter designation is returned by this method is the drive that has the <b>Enable cd writing on this drive</b> option selected. This option is found on the drive's property sheet. Only one drive on a system can have this option selected.
			

If a recordable CD drive is present but that option has been deselected, the method will return an error code.


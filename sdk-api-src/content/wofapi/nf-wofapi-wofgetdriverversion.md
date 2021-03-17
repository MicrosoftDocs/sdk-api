---
UID: NF:wofapi.WofGetDriverVersion
title: WofGetDriverVersion function (wofapi.h)
description: Used to query the version of the driver used to support a particular provider.
helpviewer_keywords: ["WofGetDriverVersion","WofGetDriverVersion function [Files]","fs.wofgetdriverversion","wofapi/WofGetDriverVersion"]
old-location: fs\wofgetdriverversion.htm
tech.root: fs
ms.assetid: F142903A-329D-40E3-A233-F013C26EC1EA
ms.date: 12/05/2018
ms.keywords: WofGetDriverVersion, WofGetDriverVersion function [Files], fs.wofgetdriverversion, wofapi/WofGetDriverVersion
req.header: wofapi.h
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
req.lib: Wofutil.lib
req.dll: Wofutil.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WofGetDriverVersion
 - wofapi/WofGetDriverVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wofutil.dll
api_name:
 - WofGetDriverVersion
---

# WofGetDriverVersion function


## -description

Used to query the version of the driver used to support a particular provider.

## -parameters

### -param FileOrVolumeHandle [in]

A handle to a file or volume opened with <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> or a similar API.

### -param Provider [in]

Indicates which provider the version query is intended for. Multiple versions of Wof may exist on the same volume at the same time for different providers.

### -param WofVersion [out]

Pointer to a ULONG which will contain the version upon successful completion of this function.

## -returns

This function returns an HRESULT indicating success or the reason for failure. If no driver is attached on the specified volume for the specified provider, the function will fail with HRESULT_FROM_WIN32(ERROR_INVALID_FUNCTION).

## -remarks

On successful completion, the WofVersion value is updated to reflect the version of the WOF driver. This value includes the major and minor version numbers of the operating system in the high-order word, and the build number of the operating system in the low-order word. The major version can be extracted with HIBYTE(HIWORD(WofVersion)); the minor version can be extracted with LOBYTE(HIWORD(WofVersion)); the build number can be extracted with LOWORD(WofVersion). 

QuickInfo

## -see-also

<a href="/windows-hardware/drivers/ifs/fsctl-get-wof-version">FSCTL_GET_WOF_VERSION</a>
---
UID: NF:mscat.IsCatalogFile
title: IsCatalogFile function (mscat.h)
description: Retrieves a Boolean value that indicates whether the specified file is a catalog file.
helpviewer_keywords: ["IsCatalogFile","IsCatalogFile function [Security]","mscat/IsCatalogFile","security.iscatalogfile"]
old-location: security\iscatalogfile.htm
tech.root: security
ms.assetid: eeba34d4-08aa-456a-8fdc-16795cbce36a
ms.date: 12/05/2018
ms.keywords: IsCatalogFile, IsCatalogFile function [Security], mscat/IsCatalogFile, security.iscatalogfile
req.header: mscat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsCatalogFile
 - mscat/IsCatalogFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - IsCatalogFile
---

# IsCatalogFile function


## -description

<p class="CCE_Message">[The  <b>IsCatalogFile</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>IsCatalogFile</b> function retrieves a Boolean value that indicates whether the specified file is a catalog file.
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.</div><div> </div>

## -parameters

### -param hFile [in, optional]

A handle to the file to check. This parameter is optional, but it must contain a valid handle if the <i>pwszFileName</i> parameter is <b>NULL</b>.

### -param pwszFileName [in, optional]

A pointer to a null-terminated wide character string that contains the name of the file to check. This parameter is optional, but it must contain a valid file name if the <i>hFile</i> parameter is <b>NULL</b>.

## -returns

Returns nonzero if the specified file is a catalog file or zero otherwise.
---
UID: NF:mscat.IsCatalogFile
title: IsCatalogFile function
author: windows-sdk-content
description: Retrieves a Boolean value that indicates whether the specified file is a catalog file.
old-location: security\iscatalogfile.htm
tech.root: seccrypto
ms.assetid: eeba34d4-08aa-456a-8fdc-16795cbce36a
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IsCatalogFile, IsCatalogFile function [Security], mscat/IsCatalogFile, security.iscatalogfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - IsCatalogFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsCatalogFile function


## -description


<p class="CCE_Message">[The  <b>IsCatalogFile</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>IsCatalogFile</b> function retrieves a Boolean value that indicates whether the specified file is a catalog file.
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.</div><div> </div>

## -parameters




### -param hFile [in, optional]

A handle to the file to check. This parameter is optional, but it must contain a valid handle if the <i>pwszFileName</i> parameter is <b>NULL</b>.


### -param pwszFileName [in, optional]

A pointer to a null-terminated wide character string that contains the name of the file to check. This parameter is optional, but it must contain a valid file name if the <i>hFile</i> parameter is <b>NULL</b>.


## -returns



Returns nonzero if the specified file is a catalog file or zero otherwise.




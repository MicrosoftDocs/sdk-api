---
UID: NF:winddi.EngDeleteFile
title: EngDeleteFile function
author: windows-sdk-content
description: The EngDeleteFile function deletes a file.
old-location: display\engdeletefile.htm
tech.root: display
ms.assetid: 2ed030cf-6d26-4bde-8d63-83fd6848ec0d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EngDeleteFile, EngDeleteFile function [Display Devices], display.engdeletefile, gdifncs_58a3395d-8a58-4a8a-b034-5dadc2dfc161.xml, winddi/EngDeleteFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngDeleteFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- EngDeleteFile
: 
---

# EngDeleteFile function


## -description


The <b>EngDeleteFile</b> function deletes a file.


## -parameters




### -param pwszFileName [in]

Pointer to a null-terminated string that contains the fully qualified name of the file to delete. An example of a fully qualified file name string is <i>L"\\??\\c:\\test.dat".</i>


## -returns



<b>EngDeleteFile</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/6887f7e1-f94f-421c-be7a-14a41d621ce1">EngMapFile</a>
 

 


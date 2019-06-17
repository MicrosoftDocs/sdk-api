---
UID: NF:oleauto.SysAllocString
title: SysAllocString function (oleauto.h)
author: windows-sdk-content
description: Allocates a new string and copies the passed string into it.
old-location: automat\sysallocstring.htm
tech.root: automat
ms.assetid: 9e0437a2-9b4a-4576-88b0-5cb9d08ca29b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SysAllocString, SysAllocString function [Automation], _oa96_SysAllocString, automat.sysallocstring, oleauto/SysAllocString
ms.topic: function
f1_keywords: ["oleauto/SysAllocString"]
req.header: oleauto.h
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SysAllocString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SysAllocString function


## -description


Allocates a new string and copies the passed string into it.


## -parameters




### -param psz [in, optional]

The string to copy.


## -returns



If successful, returns the string. If <i>psz</i> is a zero-length string, returns a zero-length <b>BSTR</b>. If <i>psz</i> is NULL or insufficient memory exists, returns NULL.





## -remarks



You can free strings created with <b>SysAllocString</b> using <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/string-manipulation-functions">String Manipulation Functions</a>
 

 


---
UID: NF:oleauto.SysAllocString
title: SysAllocString function
author: windows-sdk-content
description: Allocates a new string and copies the passed string into it.
old-location: automat\sysallocstring.htm
old-project: automat
ms.assetid: 9e0437a2-9b4a-4576-88b0-5cb9d08ca29b
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: SysAllocString, SysAllocString function [Automation], _oa96_SysAllocString, automat.sysallocstring, oleauto/SysAllocString
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: REGKIND
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
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



You can free strings created with <b>SysAllocString</b> using <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a>.




## -see-also




<a href="https://msdn.microsoft.com/323cefbf-836c-4c9d-bcbe-f2663a57d2b5">String Manipulation Functions</a>
 

 


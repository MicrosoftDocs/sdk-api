---
UID: NF:oleauto.SysStringLen
title: SysStringLen function
author: windows-sdk-content
description: Returns the length of a BSTR.
old-location: automat\sysstringlen.htm
old-project: automat
ms.assetid: 65e792af-f8a8-4cdc-a279-494bba59394a
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: SysStringLen, SysStringLen function [Automation], _oa96_SysStringLen, automat.sysstringlen, oleauto/SysStringLen
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
 - SysStringLen
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SysStringLen function


## -description


Returns the length of a BSTR.


## -parameters




### -param pbstr

TBD




#### - bstr [in, optional]

A previously allocated string.


## -returns



The number of characters in <i>bstr</i>, not including the terminating null character. If <i>bstr</i> is null the return value is zero.




## -remarks



The returned value may be different from <b>strlen</b>(bstr) if the BSTR contains embedded Null characters. This function always returns the number of characters specified in the cch parameter of the <a href="F98BFF39-BC5F-4A81-85D7-D5228E20FBC8">SysAllocStringLen</a> function used to allocate the BSTR.




## -see-also




<a href="https://msdn.microsoft.com/323cefbf-836c-4c9d-bcbe-f2663a57d2b5">String Manipulation Functions</a>
 

 


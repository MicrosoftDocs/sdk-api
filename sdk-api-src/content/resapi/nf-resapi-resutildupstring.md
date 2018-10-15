---
UID: NF:resapi.ResUtilDupString
title: ResUtilDupString function
author: windows-sdk-content
description: Duplicates a null-terminated Unicode string.
old-location: mscs\resutildupstring.htm
tech.root: mscs
ms.assetid: 7d993247-ea8c-46a0-a11e-e03b981ed4ae
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: PRESUTIL_DUP_STRING, PRESUTIL_DUP_STRING function [Failover Cluster], ResUtilDupString, ResUtilDupString function [Failover Cluster], _wolf_resutildupstring, mscs.resutildupstring, resapi/PRESUTIL_DUP_STRING, resapi/ResUtilDupString
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilDupString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilDupString function


## -description


Duplicates a null-terminated Unicode string.


## -parameters




### -param pszInString [in]

Pointer to the string to duplicate.


## -returns



If the operation succeeds, the function returns a pointer to a buffer containing the duplicate string.

If the operation fails, 
the function returns <b>NULL</b>. For more information, call the function  <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



With the  <b>ResUtilDupString</b> utility function, after using the returned string, callers should deallocate the buffer by calling the function  <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>.




## -see-also




<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>
 

 


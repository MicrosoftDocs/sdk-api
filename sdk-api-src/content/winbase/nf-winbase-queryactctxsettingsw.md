---
UID: NF:winbase.QueryActCtxSettingsW
title: QueryActCtxSettingsW function
author: windows-sdk-content
description: The QueryActCtxSettingsW function specifies the activation context, and the namespace and name of the attribute that is to be queried.
old-location: setup\queryactctxsettingsw.htm
old-project: SbsCs
ms.assetid: 80e419a5-7b57-488a-90bc-1d38d063b1ee
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: QueryActCtxSettingsW, QueryActCtxSettingsW function [Side-by-side Assemblies], setup.queryactctxsettingsw, winbase/QueryActCtxSettingsW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-sidebyside-l1-1-0.dll
-	KernelBase.dll
api_name:
-	QueryActCtxSettingsW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# QueryActCtxSettingsW function


## -description


The <b>QueryActCtxSettingsW</b> function specifies the activation context, and the namespace and name of the attribute that is to be queried.


## -parameters




### -param dwFlags [in, optional]

This value must be 0.


### -param hActCtx [in, optional]

A handle to the activation context that is being queried.


### -param settingsNameSpace [in, optional]

A pointer to a string that contains the value <b>"http://schemas.microsoft.com/SMI/2005/WindowsSettings"</b> or <b>NULL</b>. These values are equivalent.


<b>Windows 8 and Windows Server 2012:  </b>A pointer to a string that contains the value <b>"http://schemas.microsoft.com/SMI/2011/WindowsSettings"</b> is also a valid parameter.  A <b>NULL</b> is still equivalent to the previous value.




### -param settingName [in]

The name of the attribute to be queried.


### -param pvBuffer [out]

A pointer to the buffer that receives the query result.


### -param dwBuffer [in]

The size of the buffer  in characters that receives the query result.


### -param pdwWrittenOrRequired [out, optional]

A pointer to a value which is the number of characters written to the buffer specified by <i>pvBuffer</i> or that is required to hold the query result.


## -returns



If the function succeeds, it returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>.

This function sets errors that can be retrieved by calling 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. For an example, see 
<a href="https://msdn.microsoft.com/4cc626ac-7574-44ce-8377-e0bdd8e74b7e">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




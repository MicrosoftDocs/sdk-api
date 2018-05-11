---
UID: NF:winsafer.SaferIdentifyLevel
title: SaferIdentifyLevel function
author: windows-driver-content
description: Retrieves information about a level.
old-location: security\saferidentifylevel.htm
old-project: SecMgmt
ms.assetid: f82c4f40-5c37-4f97-95a2-4b2cc26bf41e
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: SaferIdentifyLevel, SaferIdentifyLevel function [Security], _mnp_saferidentifylevel, security.saferidentifylevel, winsafer/SaferIdentifyLevel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winsafer.h
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
req.typenames: SAFER_POLICY_INFO_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
api_name:
-	SaferIdentifyLevel
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SaferIdentifyLevel function


## -description


The <b>SaferIdentifyLevel</b> function retrieves information about a level.


## -parameters




### -param dwNumProperties [in]

Number of 
<a href="https://msdn.microsoft.com/039a37a9-1744-4cff-919e-e0da50d7b291">SAFER_CODE_PROPERTIES</a> structures in the <i>pCodeproperties</i>  parameter.


### -param pCodeProperties [in, optional]

Array of <a href="https://msdn.microsoft.com/039a37a9-1744-4cff-919e-e0da50d7b291">SAFER_CODE_PROPERTIES</a> structures. Each structure contains a code file to be checked and the  criteria used to check the file.


### -param pLevelHandle [out]

The returned SAFER_LEVEL_HANDLE. When you have finished using the handle, close it by calling the <a href="https://msdn.microsoft.com/8daffb35-5bb0-45b3-aff1-a8ea6a142ba5">SaferCloseLevel</a> function.


### -param lpReserved

Reserved for future use. Should be set to <b>NULL</b>.

Beginning with Windows 8 and Windows Server 2012 SRP_POLICY_APPX is defined as Windows Store app.


## -returns



<b>TRUE</b> if a SAFER_LEVEL_HANDLE was opened; otherwise,  <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




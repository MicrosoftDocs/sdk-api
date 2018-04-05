---
UID: NC:psapi.PENUM_PAGE_FILE_CALLBACKA
title: PENUM_PAGE_FILE_CALLBACKA
author: windows-driver-content
description: An application-defined callback function used with the EnumPageFiles function.
old-location: psapi\enumpagefilesproc.htm
old-project: psapi
ms.assetid: eb3610fb-2c95-4f7b-973d-8dc41d2829f1
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: EnumPageFilesProc, EnumPageFilesProc callback function [PSAPI], PENUM_PAGE_FILE_CALLBACKA, PENUM_PAGE_FILE_CALLBACKW, _win32_enumpagefilesproc, base.enumpagefilesproc, psapi.enumpagefilesproc, psapi/EnumPageFilesProc, psapi/PENUM_PAGE_FILE_CALLBACKA, psapi/PENUM_PAGE_FILE_CALLBACKW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PENUM_PAGE_FILE_CALLBACKW (Unicode) and PENUM_PAGE_FILE_CALLBACKA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSHNOTIFY, *LPPSHNOTIFY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Psapi.h
api_name:
-	EnumPageFilesProc
-	PENUM_PAGE_FILE_CALLBACKA
-	PENUM_PAGE_FILE_CALLBACKW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# PENUM_PAGE_FILE_CALLBACKA callback


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/9289fe3c-a7d9-4acb-aeb6-a50de65db0a2">EnumPageFiles</a> function.

The <b>PENUM_PAGE_FILE_CALLBACK</b> type defines a pointer to this callback function. 
<b>EnumPageFilesProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param pContext [in]

The user-defined data passed from 
<a href="https://msdn.microsoft.com/9289fe3c-a7d9-4acb-aeb6-a50de65db0a2">EnumPageFiles</a>.


### -param pPageFileInfo [in]

A pointer to an 
<a href="https://msdn.microsoft.com/020f3be8-f624-4788-8079-0f7679c9bef0">ENUM_PAGE_FILE_INFORMATION</a> structure.


### -param lpFilename [in]

The name of the pagefile.


## -returns



To continue enumeration, the callback function must return TRUE.

To stop enumeration, the callback function must return FALSE.




## -see-also




<a href="https://msdn.microsoft.com/020f3be8-f624-4788-8079-0f7679c9bef0">ENUM_PAGE_FILE_INFORMATION</a>



<a href="https://msdn.microsoft.com/9289fe3c-a7d9-4acb-aeb6-a50de65db0a2">EnumPageFiles</a>



<a href="https://msdn.microsoft.com/e158792b-fec2-498d-aae3-d5679fa55783">PSAPI Functions</a>
 

 


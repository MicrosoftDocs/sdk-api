---
UID: NF:muiload.GetUILanguageFallbackList
title: GetUILanguageFallbackList function
author: windows-driver-content
description: Gets a fallback list of UI languages represented as language names.
old-location: intl\getuilanguagefallbacklist.htm
old-project: Intl
ms.assetid: 18581fa1-f498-46ff-af83-dfbca80252e2
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetUILanguageFallbackList, GetUILanguageFallbackList function [Internationalization for Windows Applications], intl.getuilanguagefallbacklist, muiload/GetUILanguageFallbackList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: muiload.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MTP_COMMAND_DATA_OUT, *PMTP_COMMAND_DATA_OUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Muiload.lib
api_name:
-	GetUILanguageFallbackList
product: Windows
targetos: Windows
req.lib: Muiload.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# GetUILanguageFallbackList function


## -description


Gets a fallback list of UI languages represented as language names.


## -parameters




### -param pFallbackList [out, optional]

Pointer to a double null-terminated buffer in which the function retrieves an ordered, null-delimited list of language names. Alternatively, this parameter contains <b>NULL</b> if <i>cchFallbackList</i> is set to 0. In this case, the function retrieves the required size of the language buffer in <i>pcchFallbackListOut</i>.			 			 



### -param cchFallbackList [in]

Size, in characters, of the language buffer indicated by pFallbackList. Alternatively, the application can set this parameter to 0. In this case, the function retrieves the required size of the language buffer in <i>pcchFallbackListOut</i>.


### -param pcchFallbackOut

TBD




#### - pcchFallbackListOut [out, optional]

Pointer to a buffer in which the function retrieves the size of the retrieved language list. Alternatively, if <i>cchFallbackList</i> specifies 0, the function retrieves the required size of the language buffer.


## -returns



Returns <b>TRUE</b> if the function retrieves a list of fallback languages or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/2980365c-5a83-4c0f-aa37-e212ec9f0408">Multilingual User Interface</a>



<a href="https://msdn.microsoft.com/918d1f04-78fe-4b60-bee7-08d2f131437e">Multilingual User Interface Functions</a>



<a href="https://msdn.microsoft.com/ae8ab98f-dc3b-414d-85c9-6bf204c2f776">User Interface Language Management</a>
 

 


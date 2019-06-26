---
UID: NF:muiload.GetUILanguageFallbackList
title: GetUILanguageFallbackList function (muiload.h)
author: windows-sdk-content
description: Gets a fallback list of UI languages represented as language names.
old-location: intl\getuilanguagefallbacklist.htm
tech.root: Intl
ms.assetid: 18581fa1-f498-46ff-af83-dfbca80252e2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetUILanguageFallbackList, GetUILanguageFallbackList function [Internationalization for Windows Applications], intl.getuilanguagefallbacklist, muiload/GetUILanguageFallbackList
ms.topic: function
f1_keywords: 
 - "muiload/GetUILanguageFallbackList"
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
req.lib: Muiload.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Muiload.lib
api_name:
 - GetUILanguageFallbackList
product: Windows
targetos: Windows
req.typenames: 
req.redist: Muiload.lib, included in the Windows SDK for Windows 7 on Windows 2000 Professional, Windows Me/98/95
ms.custom: 19H1
---

# GetUILanguageFallbackList function


## -description


Gets a fallback list of UI languages represented as language names.


## -parameters




### -param pFallbackList [out, optional]

Pointer to a double null-terminated buffer in which the function retrieves an ordered, null-delimited list of language names. Alternatively, this parameter contains <b>NULL</b> if <i>cchFallbackList</i> is set to 0. In this case, the function retrieves the required size of the language buffer in <i>pcchFallbackListOut</i>.			 			 



### -param cchFallbackList [in]

Size, in characters, of the language buffer indicated by pFallbackList. Alternatively, the application can set this parameter to 0. In this case, the function retrieves the required size of the language buffer in <i>pcchFallbackListOut</i>.


### -param pcchFallbackOut [out, optional]

Pointer to a buffer in which the function retrieves the size of the retrieved language list. Alternatively, if <i>cchFallbackList</i> specifies 0, the function retrieves the required size of the language buffer.


## -returns



Returns <b>TRUE</b> if the function retrieves a list of fallback languages or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/multilingual-user-interface-functions">Multilingual User Interface Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/user-interface-language-management">User Interface Language Management</a>
 

 


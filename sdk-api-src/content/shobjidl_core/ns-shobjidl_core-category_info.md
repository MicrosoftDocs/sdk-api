---
UID: NS:shobjidl_core.CATEGORY_INFO
title: CATEGORY_INFO
author: windows-sdk-content
description: Contains category information. A component category is a group of logically-related Component Object Model (COM) classes that share a common category identifier (CATID).
old-location: shell\CATEGORY_INFO.htm
old-project: shell
ms.assetid: 6198cd31-94db-4d31-9cc9-f8b90e661809
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CATEGORY_INFO, CATEGORY_INFO structure [Windows Shell], inet_CATEGORY_INFO, shell.CATEGORY_INFO, shobjidl_core/CATEGORY_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CATEGORY_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	shobjidl_core.h
api_name:
-	CATEGORY_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# CATEGORY_INFO structure


## -description


Contains category information. A component category is a group of logically-related Component Object Model (COM) classes that share a common category identifier (CATID).


## -struct-fields




### -field cif

Type: <b><a href="https://msdn.microsoft.com/6179ed67-905a-454a-a226-fe1e5070e39f">CATEGORYINFO_FLAGS</a></b>

A flag from <a href="https://msdn.microsoft.com/6179ed67-905a-454a-a226-fe1e5070e39f">CATEGORYINFO_FLAGS</a> that specifies the type of information to retrieve.


### -field wszName

Type: <b>WCHAR[260]</b>

A character array that specifies the name of the category.


---
UID: NE:intshcut.translateurl_in_flags
title: translateurl_in_flags
author: windows-sdk-content
description: The TRANSLATEURL_IN_FLAGS enumerated values are used with the TranslateURL function to determine how it will execute.
old-location: shell\TRANSLATEURL_IN_FLAGS.htm
old-project: shell
ms.assetid: b04d5c7d-6d3f-4904-8de5-7586437320e9
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: TRANSLATEURL_FL_GUESS_PROTOCOL, TRANSLATEURL_FL_USE_DEFAULT_PROTOCOL, TRANSLATEURL_IN_FLAGS, TRANSLATEURL_IN_FLAGS enumeration [Windows Shell], _win32_TRANSLATEURL_IN_FLAGS, intshcut/TRANSLATEURL_FL_GUESS_PROTOCOL, intshcut/TRANSLATEURL_FL_USE_DEFAULT_PROTOCOL, intshcut/TRANSLATEURL_IN_FLAGS, shell.TRANSLATEURL_IN_FLAGS, translateurl_in_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: intshcut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRANSLATEURL_IN_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Intshcut.h
api_name:
-	TRANSLATEURL_IN_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# translateurl_in_flags enumeration


## -description


The <b>TRANSLATEURL_IN_FLAGS</b> enumerated values are used with the <a href="https://msdn.microsoft.com/2f089f5a-4d7c-4bb7-961c-5c6e3e73c7b7">TranslateURL</a> function to determine how it will execute.


## -enum-fields




### -field TRANSLATEURL_FL_GUESS_PROTOCOL

If the protocol scheme is not specified in the <i>pcszURL</i> parameter to <a href="https://msdn.microsoft.com/2f089f5a-4d7c-4bb7-961c-5c6e3e73c7b7">TranslateURL</a>, the system automatically chooses a scheme and adds it to the URL.


### -field TRANSLATEURL_FL_USE_DEFAULT_PROTOCOL

If the protocol scheme is not specified in the <i>pcszURL</i> parameter to <a href="https://msdn.microsoft.com/2f089f5a-4d7c-4bb7-961c-5c6e3e73c7b7">TranslateURL</a>, the system adds the default protocol to the URL.


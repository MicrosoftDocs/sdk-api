---
UID: NF:ole2.OleGetIconOfClass
title: OleGetIconOfClass function
author: windows-driver-content
description: Returns a handle to a metafile containing an icon and a string label for the specified CLSID.
old-location: com\olegeticonofclass.htm
old-project: com
ms.assetid: 88ac1c14-b5a8-4100-9fa5-d7af35052b48
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: OleGetIconOfClass, OleGetIconOfClass function [COM], _com_OleGetIconOfClass, com.olegeticonofclass, ole2/OleGetIconOfClass
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: QACONTROL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
-	Ext-MS-Win-Com-OLE32-l1-1-3.dll
-	Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
-	OleGetIconOfClass
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OleGetIconOfClass function


## -description


Returns a handle to a metafile containing an icon and a string label for the specified CLSID.


## -parameters




### -param rclsid [in]

The CLSID for which the icon and string are to be requested.


### -param lpszLabel [in, optional]

A pointer to the label for the icon.


### -param fUseTypeAsLabel [in]

Indicates whether to use the user type string in the CLSID as the icon label.


## -returns



If the function succeeds, the return value is a handle to a metafile that contains and icon and label for the specified CLSID. Otherwise, the function returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/2fa9cd75-4dc6-45a3-aa62-e82bd28289a5">OleGetIconOfFile</a>



<a href="https://msdn.microsoft.com/627a79eb-46dd-4df7-a0d6-cab37b73387a">OleMetafilePictFromIconAndLabel</a>
 

 


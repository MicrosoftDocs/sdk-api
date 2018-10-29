---
UID: NS:shtypes._SHELLDETAILS
title: "_SHELLDETAILS"
author: windows-sdk-content
description: Reports detailed information on an item in a Shell folder.
old-location: shell\SHELLDETAILS_str.htm
tech.root: shell
ms.assetid: 2910debb-b769-4498-bd99-9fbf16567e15
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*LPSHELLDETAILS, LPSHELLDETAILS, LPSHELLDETAILS structure pointer [Windows Shell], LVCFMT_CENTER, LVCFMT_COL_HAS_IMAGES, LVCFMT_LEFT, LVCFMT_RIGHT, SHELLDETAILS, SHELLDETAILS structure [Windows Shell], The alignment of the leftmost column is always left-justified and cannot be changed., _SHELLDETAILS, _win32_SHELLDETAILS_str, shell.SHELLDETAILS_str, shtypes/LPSHELLDETAILS, shtypes/SHELLDETAILS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shtypes.h
api_name:
 - SHELLDETAILS
product: Windows
targetos: Windows
req.typenames: SHELLDETAILS, *LPSHELLDETAILS
req.redist: 
---

# _SHELLDETAILS structure


## -description


Reports detailed information on an item in a Shell folder.


## -struct-fields




### -field fmt

Type: <b>int</b>

The alignment of the column heading and the subitem text in the column. This member can be one of the following values.



#### LVCFMT_CENTER

Text is centered.



#### LVCFMT_COL_HAS_IMAGES


<a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 4.70</a>. Header item contains an image in the image list.



#### LVCFMT_LEFT

Text is left-aligned.



#### LVCFMT_RIGHT

Text is right-aligned.



##### 


### -field cxChar

Type: <b>int</b>

The number of average-sized characters in the header.


### -field str

Type: <b><a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a></b>

An <a href="https://msdn.microsoft.com/7868ef9b-07db-455b-b0be-ef0db7891447">STRRET</a> structure that includes a string with the requested information. To convert this structure to a string, use <a href="https://msdn.microsoft.com/89dab3ee-e9f8-499a-97ec-6fe732315891">StrRetToBuf</a> or <a href="https://msdn.microsoft.com/03b0dffb-8ef7-41da-9773-81ed55275802">StrRetToStr</a>.


## -see-also




<a href="https://msdn.microsoft.com/5442dc80-9ecf-4e47-a84d-6da4327696ef">IShellDetails::GetDetailsOf</a>
 

 


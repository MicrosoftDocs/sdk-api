---
UID: NF:shlobj_core.GetIconLocation
title: GetIconLocation function
author: windows-driver-content
description: Gets the location of the icon assigned to the link.
old-location: shell\ShellLinkObject_GetIconLocation.htm
old-project: shell
ms.assetid: 3bb7f0f0-7ab9-41e6-b738-274efbcd52ab
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetIconLocation, GetIconLocation method [Windows Shell], GetIconLocation method [Windows Shell], ShellLinkObject object, ShellLinkObject object [Windows Shell], GetIconLocation method, _win32_ShellLinkObject_GetIconLocation, shell.ShellLinkObject_GetIconLocation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shldisp.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	ShellLinkObject.GetIconLocation
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# GetIconLocation function


## -description


Gets the location of the icon assigned to the link.


## -parameters




### -param uFlags

TBD


### -param pszIconFile

TBD


### -param cchMax

TBD


### -param piIndex

TBD


### -param pwFlags

TBD




#### - sPath [out]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a>*</b>

When this method returns, it holds the fully qualified path of the file that contains the icon.


## -returns



Type: <b>Integer*</b>

Returns the icon's index in the file specified by <i>sPath</i>.




## -see-also




<a href="https://msdn.microsoft.com/257bb8e2-29fa-4d2f-ac2d-3497cf12959c">SetIconLocation</a>



<a href="https://msdn.microsoft.com/d3c0ccf8-0f83-42f7-9d6f-1fb293da6364">ShellLinkObject</a>
 

 


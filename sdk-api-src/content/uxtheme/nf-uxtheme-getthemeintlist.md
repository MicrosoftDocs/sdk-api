---
UID: NF:uxtheme.GetThemeIntList
title: GetThemeIntList function
author: windows-sdk-content
description: Retrieves a list of int data from a visual style.
old-location: controls\GetThemeIntList.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemeintlist.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetThemeIntList, GetThemeIntList function [Windows Controls], controls.GetThemeIntList, controls.inet_GetThemeIntList, inet_GetThemeIntList, inet_GetThemeIntList_cpp, uxtheme/GetThemeIntList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: UxTheme.lib
req.dll: UxTheme.dll (version 1.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - GetThemeIntList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetThemeIntList function


## -description


Retrieves a list of <b>int</b> data from a visual style.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/3c496a3f-e4d0-4938-af66-85df93829cd8">OpenThemeData</a> to create an HTHEME.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the list of data to return. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param iPropId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the property to retrieve. See <a href="https://msdn.microsoft.com/b0e22022-fea9-43d1-8ef0-7a1c518760f1">Property Identifiers</a>.


### -param pIntList [out]

Type: <b><a href="https://msdn.microsoft.com/2242d739-a7d8-4478-adb4-7d4bc264554f">INTLIST</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/2242d739-a7d8-4478-adb4-7d4bc264554f">INTLIST</a> structure that receives the <b>int</b> data.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful, otherwise an error code.




## -see-also




<a href="https://msdn.microsoft.com/2242d739-a7d8-4478-adb4-7d4bc264554f">INTLIST</a>
 

 


---
UID: NF:uxtheme.GetThemeIntList
title: GetThemeIntList function (uxtheme.h)
author: windows-sdk-content
description: Retrieves a list of int data from a visual style.
old-location: controls\GetThemeIntList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemeintlist.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetThemeIntList, GetThemeIntList function [Windows Controls], controls.GetThemeIntList, controls.inet_GetThemeIntList, inet_GetThemeIntList, inet_GetThemeIntList_cpp, uxtheme/GetThemeIntList
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
ms.custom: 19H1
---

# GetThemeIntList function


## -description


Retrieves a list of <b>int</b> data from a visual style.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/en-us/library/Bb759821(v=VS.85).aspx">OpenThemeData</a> to create an HTHEME.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the list of data to return. See <a href="https://msdn.microsoft.com/en-us/library/Bb773210(v=VS.85).aspx">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="https://msdn.microsoft.com/en-us/library/Bb773210(v=VS.85).aspx">Parts and States</a>.


### -param iPropId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the property to retrieve. See <a href="https://msdn.microsoft.com/en-us/library/Bb773213(v=VS.85).aspx">Property Identifiers</a>.


### -param pIntList [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb773240(v=VS.85).aspx">INTLIST</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb773240(v=VS.85).aspx">INTLIST</a> structure that receives the <b>int</b> data.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful, otherwise an error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb773240(v=VS.85).aspx">INTLIST</a>
 

 


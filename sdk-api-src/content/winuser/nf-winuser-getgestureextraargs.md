---
UID: NF:winuser.GetGestureExtraArgs
title: GetGestureExtraArgs function
author: windows-sdk-content
description: Retrieves additional information about a gesture from its GESTUREINFO handle.
old-location: wintouch\getgestureextraargs.htm
old-project: wintouch
ms.assetid: f7775d88-6a5b-4283-ab40-65c2da218f81
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: GetGestureExtraArgs, GetGestureExtraArgs function [Windows Touch], wintouch.getgestureextraargs, winuser/GetGestureExtraArgs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
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
tech.root: 
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	user32.dll
api_name:
-	GetGestureExtraArgs
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetGestureExtraArgs function


## -description


Retrieves additional information about a gesture from its <a href="https://msdn.microsoft.com/f5b8b530-ff1e-4d78-a12f-86990fe9ac88">GESTUREINFO</a> handle.


## -parameters




### -param hGestureInfo [in]

The handle to the gesture information that is passed in the <i>lParam</i> of a <a href="https://msdn.microsoft.com/4167aeb0-2c31-4b7b-ad1b-e6d37da09ef8">WM_GESTURE</a> message.


### -param cbExtraArgs [in]

A count of the bytes of data stored in the extra arguments.


### -param pExtraArgs [out]

A pointer to the extra argument information.


## -returns



If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="http://msdn.microsoft.com/en-us/library/ms679360.aspx">GetLastError</a> function.




## -remarks



This function is reserved for future use and should only be used for testing. Windows 7 gestures do not use extra arguments.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/407ed585-09aa-4174-8907-8bb9590f1795">GetGestureInfo</a>



<a href="https://msdn.microsoft.com/afd61b18-4e54-44c5-9b71-74908c76c7ac">Programming Guide for Gestures</a>
 

 


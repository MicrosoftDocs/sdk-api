---
UID: NF:uiautomationcoreapi.TransformPattern_Rotate
title: TransformPattern_Rotate function
author: windows-sdk-content
description: Rotates an element on the screen.
old-location: winauto\uiauto_TransformPattern_RotateConPat.htm
old-project: WinAuto
ms.assetid: c3c61c67-7c4a-4211-90f9-b5000a4938a3
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: TransformPattern_Rotate, TransformPattern_Rotate function [Windows Accessibility], uiauto.uiauto_TransformPattern_RotateConPat, uiauto_TransformPattern_RotateConPat, uiautomationcoreapi/TransformPattern_Rotate, winauto.uiauto_TransformPattern_RotateConPat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Uiautomationcore.dll
api_name:
-	TransformPattern_Rotate
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TransformPattern_Rotate function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Rotates an element on the screen.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.


### -param degrees [in]

Type: <b>double</b>

The number of degrees to rotate the control. 
				Positive values are clockwise; negative values are counterclockwise.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




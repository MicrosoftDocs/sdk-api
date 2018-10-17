---
UID: NF:uiautomationcoreapi.UiaNodeFromPoint
title: UiaNodeFromPoint function
author: windows-sdk-content
description: Retrieves the UI Automation node for the element at the specified point.
old-location: winauto\uiauto_UiaNodeFromPointFunction.htm
tech.root: WinAuto
ms.assetid: 46da2f6a-3cb7-4220-b578-4fcf9711b99f
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: UiaNodeFromPoint, UiaNodeFromPoint function [Windows Accessibility], uiauto.uiauto_UiaNodeFromPointFunction, uiauto_UiaNodeFromPointFunction, uiautomationcoreapi/UiaNodeFromPoint, winauto.uiauto_UiaNodeFromPointFunction
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - UiaNodeFromPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaNodeFromPoint function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Retrieves the UI Automation node for the element at the specified point.


## -parameters




### -param x [in]

Type: <b>double</b>

The horizontal coordinate of the point.


### -param y [in]

Type: <b>double</b>

The vertical coordinate of the point.


### -param pRequest [in]

Type: <b><a href="https://msdn.microsoft.com/426355e4-50ce-4189-824d-c2256903224c">UiaCacheRequest</a>*</b>

The address of a <a href="https://msdn.microsoft.com/426355e4-50ce-4189-824d-c2256903224c">UiaCacheRequest</a> structure that contains the cache request for information from the client.


### -param ppRequestedData [out]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

The address of a variable that receives a pointer to a <a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> that contains the requested data. This parameter is passed uninitialized.


### -param ppTreeStructure [out]

Type: <b>BSTR*</b>

The address of a variable that receives the description of the tree structure.
				This parameter is passed uninitialized. See Remarks.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




## -remarks



The element returned will be the closest element in the UI Automation tree structure that matches the specified criteria.

The tree structure is described by a string where every character is either "p" or ")". 
			The first character in the string always represents the root node. 
The string is <b>NULL</b> if no elements are returned by the function.
			

A "p" represents a node 
			(UI Automation element). When one "p" directly follows another, the second node is a child of the first.
			A ")" represents a step back up the tree. For example, "pp)p" represents a node followed
			by two child nodes that are siblings of one another. In "pp))p", the last node is a sibling of the first one.
			




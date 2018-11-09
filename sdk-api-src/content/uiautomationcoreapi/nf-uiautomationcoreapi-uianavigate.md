---
UID: NF:uiautomationcoreapi.UiaNavigate
title: UiaNavigate function
author: windows-sdk-content
description: Navigates in the UI Automation tree, optionally retrieving cached information.
old-location: winauto\uiauto_UiaNavigateAutoMeth.htm
tech.root: WinAuto
ms.assetid: 11f0d52a-11be-4038-bf9e-94e44b118a22
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: UiaNavigate, UiaNavigate function [Windows Accessibility], uiauto.uiauto_UiaNavigateAutoMeth, uiauto_UiaNavigateAutoMeth, uiautomationcoreapi/UiaNavigate, winauto.uiauto_UiaNavigateAutoMeth
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
 - UiaNavigate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaNavigate function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Navigates in the UI Automation tree, optionally retrieving cached information.


## -parameters




### -param hnode [in]

Type: <b>HUIANODE</b>

The element on which the navigation begins.


### -param direction [in]

Type: <b><a href="https://msdn.microsoft.com/33385413-3500-4f80-b53a-fe960d1b53ee">NavigateDirection</a></b>

A value from the <a href="https://msdn.microsoft.com/33385413-3500-4f80-b53a-fe960d1b53ee">NavigateDirection</a> enumerated type indicating the direction to navigate from <i>hnode</i>.


### -param pCondition [in]

Type: <b><a href="https://msdn.microsoft.com/82b5db01-08c9-4518-9d33-15d7813d0c80">UiaCondition</a>*</b>

The address of a <a href="https://msdn.microsoft.com/82b5db01-08c9-4518-9d33-15d7813d0c80">UiaCondition</a> structure that specifies the condition that the element being navigated to must match. Use this parameter to skip elements that are not of interest.


### -param pRequest [in]

Type: <b><a href="https://msdn.microsoft.com/426355e4-50ce-4189-824d-c2256903224c">UiaCacheRequest</a>*</b>

The address of a <a href="https://msdn.microsoft.com/426355e4-50ce-4189-824d-c2256903224c">UiaCacheRequest</a> structure that contains a description of the information to be cached.


### -param ppRequestedData [out]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

The address of a variable that receives a pointer to a <a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> that contains the requested data. This parameter is passed uninitialized. See Remarks.


### -param ppTreeStructure [out]

Type: <b>BSTR*</b>

The address of a variable that receives the description of the tree structure. 
				This parameter is passed uninitialized. See Remarks.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




## -remarks



The tree structure is described by a string where every character is either "p" or ")". 
			The first character in the string always represents the root node. 
The string is <b>NULL</b> if no elements are returned by the function.
			

A "p" represents a node 
			(UI Automation element). When one "p" directly follows another, the second node is a child of the first.
			A ")" represents a step back up the tree. For example, "pp)p" represents a node followed
			by two child nodes that are siblings of one another. In "pp))p", the last node is a sibling of the first one.




---
UID: NF:uiautomationcoreapi.UiaNavigate
title: UiaNavigate function (uiautomationcoreapi.h)
description: Navigates in the UI Automation tree, optionally retrieving cached information.
helpviewer_keywords: ["UiaNavigate","UiaNavigate function [Windows Accessibility]","uiauto.uiauto_UiaNavigateAutoMeth","uiauto_UiaNavigateAutoMeth","uiautomationcoreapi/UiaNavigate","winauto.uiauto_UiaNavigateAutoMeth"]
old-location: winauto\uiauto_UiaNavigateAutoMeth.htm
tech.root: WinAuto
ms.assetid: 11f0d52a-11be-4038-bf9e-94e44b118a22
ms.date: 12/05/2018
ms.keywords: UiaNavigate, UiaNavigate function [Windows Accessibility], uiauto.uiauto_UiaNavigateAutoMeth, uiauto_UiaNavigateAutoMeth, uiautomationcoreapi/UiaNavigate, winauto.uiauto_UiaNavigateAutoMeth
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaNavigate
 - uiautomationcoreapi/UiaNavigate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - UiaNavigate
---

# UiaNavigate function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Navigates in the UI Automation tree, optionally retrieving cached information.

## -parameters

### -param hnode [in]

Type: <b>HUIANODE</b>

The element on which the navigation begins.

### -param direction [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-navigatedirection">NavigateDirection</a></b>

A value from the <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-navigatedirection">NavigateDirection</a> enumerated type indicating the direction to navigate from <i>hnode</i>.

### -param pCondition [in]

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiacondition">UiaCondition</a>*</b>

The address of a <a href="/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiacondition">UiaCondition</a> structure that specifies the condition that the element being navigated to must match. Use this parameter to skip elements that are not of interest.

### -param pRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiacacherequest">UiaCacheRequest</a>*</b>

The address of a <a href="/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiacacherequest">UiaCacheRequest</a> structure that contains a description of the information to be cached.

### -param ppRequestedData [out]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

The address of a variable that receives a pointer to a <a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> that contains the requested data. This parameter is passed uninitialized. See Remarks.

### -param ppTreeStructure [out]

Type: <b>BSTR*</b>

The address of a variable that receives the description of the tree structure. 
				This parameter is passed uninitialized. See Remarks.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

## -remarks

The tree structure is described by a string where every character is either "p" or ")". 
			The first character in the string always represents the root node. 
The string is <b>NULL</b> if no elements are returned by the function.
			

A "p" represents a node 
			(UI Automation element). When one "p" directly follows another, the second node is a child of the first.
			A ")" represents a step back up the tree. For example, "pp)p" represents a node followed
			by two child nodes that are siblings of one another. In "pp))p", the last node is a sibling of the first one.
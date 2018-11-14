---
UID: NF:uiautomationcoreapi.UiaGetUpdatedCache
title: UiaGetUpdatedCache function
author: windows-sdk-content
description: Updates the cache of property values and control patterns.
old-location: winauto\uiauto_UiaGetUpdatedCacheAutoMeth.htm
tech.root: WinAuto
ms.assetid: 06f0874d-ca25-4fa8-8cbc-96c1eee1b36c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: UiaGetUpdatedCache, UiaGetUpdatedCache function [Windows Accessibility], uiauto.uiauto_UiaGetUpdatedCacheAutoMeth, uiauto_UiaGetUpdatedCacheAutoMeth, uiautomationcoreapi/UiaGetUpdatedCache, winauto.uiauto_UiaGetUpdatedCacheAutoMeth
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
 - UiaGetUpdatedCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- UiaGetUpdatedCache
: 
---

# UiaGetUpdatedCache function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Updates the cache of property values and control patterns.


## -parameters




### -param hnode [in]

Type: <b>HUIANODE</b>

The element that updated information is being requested for.


### -param pRequest [in]

Type: <b><a href="https://msdn.microsoft.com/426355e4-50ce-4189-824d-c2256903224c">UiaCacheRequest</a>*</b>

The address of a <a href="https://msdn.microsoft.com/426355e4-50ce-4189-824d-c2256903224c">UiaCacheRequest</a> structure that specifies the cached information to update.


### -param normalizeState [in]

Type: <b><a href="https://msdn.microsoft.com/242b3770-1082-4df9-b21b-cc78e587a2b5">NormalizeState</a></b>

A value from the <a href="https://msdn.microsoft.com/242b3770-1082-4df9-b21b-cc78e587a2b5">NormalizeState</a> enumerated type specifying the type of normalization.


### -param pNormalizeCondition [in]

Type: <b><a href="https://msdn.microsoft.com/82b5db01-08c9-4518-9d33-15d7813d0c80">UiaCondition</a>*</b>

The address of a <a href="https://msdn.microsoft.com/82b5db01-08c9-4518-9d33-15d7813d0c80">UiaCondition</a> structure that specifies a condition against which the information can be normalized, if <i>normalizeState</i> is <a href="uiauto_NormalizeStateEnum.htm">NormalizeState_Custom</a>.


### -param ppRequestedData [out]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

The address of a variable that receives a pointer to a <a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> that contains the requested data. This parameter is passed uninitialized. See Remarks.


### -param ppTreeStructure [out]

Type: <b>BSTR*</b>

A pointer to the description of the tree structure.
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




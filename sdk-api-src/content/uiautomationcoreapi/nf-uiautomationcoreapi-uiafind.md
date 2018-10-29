---
UID: NF:uiautomationcoreapi.UiaFind
title: UiaFind function
author: windows-sdk-content
description: Retrieves one or more UI Automation nodes that match the search criteria.
old-location: winauto\uiauto_UiaFindAutoMeth.htm
tech.root: WinAuto
ms.assetid: fe86b393-9c8d-46f1-85dc-5ac37f423ce0
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: UiaFind, UiaFind function [Windows Accessibility], uiauto.uiauto_UiaFindAutoMeth, uiauto_UiaFindAutoMeth, uiautomationcoreapi/UiaFind, winauto.uiauto_UiaFindAutoMeth
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
 - UiaFind
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaFind function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Retrieves one or more UI Automation nodes that match the search criteria.


## -parameters




### -param hnode [in]

Type: <b>HUIANODE</b>

The node to use as starting-point of the search.


### -param pParams [in]

Type: <b><a href="https://msdn.microsoft.com/eb3c16d1-3e64-4f8e-aa03-c72c7a87b67f">UiaFindParams</a>*</b>

The address of a <a href="https://msdn.microsoft.com/eb3c16d1-3e64-4f8e-aa03-c72c7a87b67f">UiaFindParams</a> structure that contains the search parameters.


### -param pRequest [in]

Type: <b><a href="https://msdn.microsoft.com/426355e4-50ce-4189-824d-c2256903224c">UiaCacheRequest</a>*</b>

The address of a <a href="https://msdn.microsoft.com/426355e4-50ce-4189-824d-c2256903224c">UiaCacheRequest</a> structure that specifies what information is to be cached.


### -param ppRequestedData [out]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

The address of a variable that receives a pointer to a <a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> containing the requested data. This parameter is passed uninitialized. See Remarks. 


### -param ppOffsets [out]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

The address of a variable that receives a pointer to a SAFEARRAY containing the indexes to the requested data array for where the element subtree starts. This parameter is passed uninitialized.


### -param ppTreeStructures [out]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

The address of a variable that receives a pointer to a SAFEARRAY containing the description of the tree structure. This parameter is passed uninitialized. See Remarks.


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
			




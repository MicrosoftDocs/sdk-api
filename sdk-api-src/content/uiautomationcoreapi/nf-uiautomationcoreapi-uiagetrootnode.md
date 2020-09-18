---
UID: NF:uiautomationcoreapi.UiaGetRootNode
title: UiaGetRootNode function (uiautomationcoreapi.h)
description: Retrieves the root UI Automation node.
helpviewer_keywords: ["UiaGetRootNode","UiaGetRootNode function [Windows Accessibility]","uiauto.uiauto_UiaGetRootNodeFunction","uiauto_UiaGetRootNodeFunction","uiautomationcoreapi/UiaGetRootNode","winauto.uiauto_UiaGetRootNodeFunction"]
old-location: winauto\uiauto_UiaGetRootNodeFunction.htm
tech.root: WinAuto
ms.assetid: 14296fec-1b03-408c-ba96-9429107df592
ms.date: 12/05/2018
ms.keywords: UiaGetRootNode, UiaGetRootNode function [Windows Accessibility], uiauto.uiauto_UiaGetRootNodeFunction, uiauto_UiaGetRootNodeFunction, uiautomationcoreapi/UiaGetRootNode, winauto.uiauto_UiaGetRootNodeFunction
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
 - UiaGetRootNode
 - uiautomationcoreapi/UiaGetRootNode
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
 - UiaGetRootNode
---

# UiaGetRootNode function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Retrieves the root UI Automation node.

## -parameters

### -param phnode [out]

Type: <b>HUIANODE*</b>

The address of a variable that receives a handle to the root node.
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.
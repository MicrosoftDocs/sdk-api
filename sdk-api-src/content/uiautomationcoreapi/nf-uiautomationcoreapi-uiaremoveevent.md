---
UID: NF:uiautomationcoreapi.UiaRemoveEvent
title: UiaRemoveEvent function (uiautomationcoreapi.h)
description: Removes a listener for events on a node in the UI Automation tree.
helpviewer_keywords: ["UiaRemoveEvent","UiaRemoveEvent function [Windows Accessibility]","uiauto.uiauto_UiaRemoveEventClientEvent","uiauto_UiaRemoveEventClientEvent","uiautomationcoreapi/UiaRemoveEvent","winauto.uiauto_UiaRemoveEventClientEvent"]
old-location: winauto\uiauto_UiaRemoveEventClientEvent.htm
tech.root: WinAuto
ms.assetid: c98b3e0f-c3d3-45a5-b1a1-80da1b5673f3
ms.date: 12/05/2018
ms.keywords: UiaRemoveEvent, UiaRemoveEvent function [Windows Accessibility], uiauto.uiauto_UiaRemoveEventClientEvent, uiauto_UiaRemoveEventClientEvent, uiautomationcoreapi/UiaRemoveEvent, winauto.uiauto_UiaRemoveEventClientEvent
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
 - UiaRemoveEvent
 - uiautomationcoreapi/UiaRemoveEvent
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
 - UiaRemoveEvent
---

# UiaRemoveEvent function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Removes a listener for events on a node in the UI Automation tree.

## -parameters

### -param hEvent [in]

Type: <b>HUIAEVENT</b>

The event to remove. This value was retrieved from <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaaddevent">UiaAddEvent</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

## -remarks

The callback pointer, the scope, the node, and the list of properties must match exactly the parameters that were sent to the 
corresponding <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaaddevent">UiaAddEvent</a>.
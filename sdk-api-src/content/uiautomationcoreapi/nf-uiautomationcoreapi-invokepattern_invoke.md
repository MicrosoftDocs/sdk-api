---
UID: NF:uiautomationcoreapi.InvokePattern_Invoke
title: InvokePattern_Invoke function (uiautomationcoreapi.h)
description: Sends a request to activate a control and initiate its single, unambiguous action. (InvokePattern_Invoke)
helpviewer_keywords: ["InvokePattern_Invoke","InvokePattern_Invoke function [Windows Accessibility]","uiauto.uiauto_InvokePattern_InvokeConPat","uiauto_InvokePattern_InvokeConPat","uiautomationcoreapi/InvokePattern_Invoke","winauto.uiauto_InvokePattern_InvokeConPat"]
old-location: winauto\uiauto_InvokePattern_InvokeConPat.htm
tech.root: WinAuto
ms.assetid: 3677b34f-31fe-4e28-a768-a79082e63722
ms.date: 12/05/2018
ms.keywords: InvokePattern_Invoke, InvokePattern_Invoke function [Windows Accessibility], uiauto.uiauto_InvokePattern_InvokeConPat, uiauto_InvokePattern_InvokeConPat, uiautomationcoreapi/InvokePattern_Invoke, winauto.uiauto_InvokePattern_InvokeConPat
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
 - InvokePattern_Invoke
 - uiautomationcoreapi/InvokePattern_Invoke
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
 - InvokePattern_Invoke
---

# InvokePattern_Invoke function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Sends a request to activate a control and initiate its single, unambiguous action.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The <i>control pattern</i> object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

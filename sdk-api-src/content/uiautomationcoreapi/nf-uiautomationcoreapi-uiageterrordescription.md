---
UID: NF:uiautomationcoreapi.UiaGetErrorDescription
title: UiaGetErrorDescription function (uiautomationcoreapi.h)
description: Gets an error string so that it can be passed to the client. This method is not used directly by clients.
helpviewer_keywords: ["UiaGetErrorDescription","UiaGetErrorDescription function [Windows Accessibility]","uiauto.uiauto_UiaGetErrorDescriptionAutoMeth","uiauto_UiaGetErrorDescriptionAutoMeth","uiautomationcoreapi/UiaGetErrorDescription","winauto.uiauto_UiaGetErrorDescriptionAutoMeth"]
old-location: winauto\uiauto_UiaGetErrorDescriptionAutoMeth.htm
tech.root: WinAuto
ms.assetid: bb00f7cd-8557-4ef7-a53c-c020d0acdb78
ms.date: 12/05/2018
ms.keywords: UiaGetErrorDescription, UiaGetErrorDescription function [Windows Accessibility], uiauto.uiauto_UiaGetErrorDescriptionAutoMeth, uiauto_UiaGetErrorDescriptionAutoMeth, uiautomationcoreapi/UiaGetErrorDescription, winauto.uiauto_UiaGetErrorDescriptionAutoMeth
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
 - UiaGetErrorDescription
 - uiautomationcoreapi/UiaGetErrorDescription
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
 - UiaGetErrorDescription
---

# UiaGetErrorDescription function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Gets an error string so that it can be passed to the client. 
		This method is not used directly by clients.

## -parameters

### -param pDescription [out]

Type: <b>BSTR*</b>

The address of a variable that receives the description of the error. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if an error description can be reported; otherwise <b>FALSE</b>.
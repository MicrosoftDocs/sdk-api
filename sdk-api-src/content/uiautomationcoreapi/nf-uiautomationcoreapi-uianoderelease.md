---
UID: NF:uiautomationcoreapi.UiaNodeRelease
title: UiaNodeRelease function (uiautomationcoreapi.h)
description: Deletes a node from memory.
helpviewer_keywords: ["UiaNodeRelease","UiaNodeRelease function [Windows Accessibility]","uiauto.uiauto_UiaNodeReleaseMemManMeth","uiauto_UiaNodeReleaseMemManMeth","uiautomationcoreapi/UiaNodeRelease","winauto.uiauto_UiaNodeReleaseMemManMeth"]
old-location: winauto\uiauto_UiaNodeReleaseMemManMeth.htm
tech.root: WinAuto
ms.assetid: dce9fd8a-b307-46b6-9e1d-ee31904e383f
ms.date: 12/05/2018
ms.keywords: UiaNodeRelease, UiaNodeRelease function [Windows Accessibility], uiauto.uiauto_UiaNodeReleaseMemManMeth, uiauto_UiaNodeReleaseMemManMeth, uiautomationcoreapi/UiaNodeRelease, winauto.uiauto_UiaNodeReleaseMemManMeth
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
 - UiaNodeRelease
 - uiautomationcoreapi/UiaNodeRelease
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
 - UiaNodeRelease
---

# UiaNodeRelease function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Deletes a node from memory.

## -parameters

### -param hnode [in]

Type: <b>HUIANODE</b>

The node to be deleted.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the node was successfully deleted; otherwise <b>FALSE</b>.
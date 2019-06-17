---
UID: NC:prsht.LPFNADDPROPSHEETPAGE
title: LPFNADDPROPSHEETPAGE (prsht.h)
author: windows-sdk-content
description: Specifies an application-defined callback function that a property sheet extension uses to add a page to a property sheet.
old-location: controls\AddPropSheetPageProc.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\functions\addpropsheetpageproc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddPropSheetPageProc, AddPropSheetPageProc callback, AddPropSheetPageProc callback function [Windows Controls], LPFNADDPROPSHEETPAGE, _win32_AddPropSheetPageProc, _win32_AddPropSheetPageProc_cpp, controls.AddPropSheetPageProc, controls._win32_AddPropSheetPageProc, prsht/AddPropSheetPageProc, prsht/LPFNADDPROPSHEETPAGE
ms.topic: callback
f1_keywords: ["prsht/AddPropSheetPageProc"]
req.header: prsht.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Prsht.h
api_name:
 - AddPropSheetPageProc
 - LPFNADDPROPSHEETPAGE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LPFNADDPROPSHEETPAGE callback function


## -description


Specifies an application-defined callback function that a property sheet extension uses to add a page to a property sheet.


## -parameters




### -param Arg1


### -param Arg2








#### - hpage

Type: <b>HPROPSHEETPAGE</b>

Handle to a property sheet page.


#### - lParam

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Application-defined 32-bit value.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



<div class="alert"><b>Note</b>  This function is not supported when using the Aero wizard style (<a href="https://docs.microsoft.com/windows/desktop/api/prsht/ns-prsht-_propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>



---
UID: NC:prsht.LPFNADDPROPSHEETPAGE
title: LPFNADDPROPSHEETPAGE
author: windows-sdk-content
description: Specifies an application-defined callback function that a property sheet extension uses to add a page to a property sheet.
old-location: controls\AddPropSheetPageProc.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\propsheet\functions\addpropsheetpageproc.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: AddPropSheetPageProc, AddPropSheetPageProc callback, AddPropSheetPageProc callback function [Windows Controls], LPFNADDPROPSHEETPAGE, _win32_AddPropSheetPageProc, _win32_AddPropSheetPageProc_cpp, controls.AddPropSheetPageProc, controls._win32_AddPropSheetPageProc, prsht/AddPropSheetPageProc, prsht/LPFNADDPROPSHEETPAGE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Application-defined 32-bit value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



<div class="alert"><b>Note</b>  This function is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PSH_AEROWIZARD</a>).</div>
<div> </div>



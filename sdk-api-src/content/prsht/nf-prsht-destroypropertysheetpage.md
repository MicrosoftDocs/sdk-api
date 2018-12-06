---
UID: NF:prsht.DestroyPropertySheetPage
title: DestroyPropertySheetPage function
author: windows-sdk-content
description: Destroys a property sheet page. An application must call this function for pages that have not been passed to the PropertySheet function.
old-location: controls\DestroyPropertySheetPage.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\propsheet\functions\destroypropertysheetpage.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DestroyPropertySheetPage, DestroyPropertySheetPage function [Windows Controls], _win32_DestroyPropertySheetPage, _win32_DestroyPropertySheetPage_cpp, controls.DestroyPropertySheetPage, controls._win32_DestroyPropertySheetPage, prsht/DestroyPropertySheetPage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DestroyPropertySheetPage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DestroyPropertySheetPage function


## -description


Destroys a property sheet page. An application must call this function for pages that have not been passed to the <a href="https://msdn.microsoft.com/1cef9b14-498e-4dcb-94a5-5faa17e0774e">PropertySheet</a> function.


## -parameters




### -param Arg1

Type: <b>HPROPSHEETPAGE</b>

Handle to the property sheet page to delete.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.




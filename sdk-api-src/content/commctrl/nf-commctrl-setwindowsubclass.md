---
UID: NF:commctrl.SetWindowSubclass
title: SetWindowSubclass function
author: windows-sdk-content
description: Installs or updates a window subclass callback.
old-location: shell\SetWindowSubclass.htm
tech.root: shell
ms.assetid: 0b11144d-eb4e-462c-96d3-38c4bac48f2a
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: SetWindowSubclass, SetWindowSubclass function [Windows Shell], commctrl/SetWindowSubclass, inet_SetWindowSubclass, shell.SetWindowSubclass
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: commctrl.h
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 5.8 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - SetWindowSubclass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetWindowSubclass function


## -description


Installs or updates a window subclass callback.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

The handle of the window being subclassed.


### -param pfnSubclass [in]

Type: <b><a href="https://msdn.microsoft.com/44e4cbe0-8252-4bcc-885e-d8af856e8ad7">SUBCLASSPROC</a></b>

A pointer to a window procedure. This pointer and the subclass ID uniquely identify this subclass callback. For the callback function prototype, see <a href="https://msdn.microsoft.com/44e4cbe0-8252-4bcc-885e-d8af856e8ad7">SUBCLASSPROC</a>.


### -param uIdSubclass [in]

Type: <b>UINT_PTR</b>

The subclass ID. This ID together with the subclass procedure uniquely identify a subclass. To remove a subclass, pass the subclass procedure and this value to the <a href="https://msdn.microsoft.com/en-us/library/Bb762094(v=VS.85).aspx">RemoveWindowSubclass</a> function. This value is passed to the subclass procedure in the uIdSubclass parameter.


### -param dwRefData [in]

Type: <b>DWORD_PTR</b>

<b>DWORD_PTR</b> to reference data. The meaning of this value is determined by the calling application. This value is passed to the subclass procedure in the dwRefData parameter. A different dwRefData is associated with each combination of window handle, subclass procedure and uIdSubclass.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if the subclass callback was successfully installed; otherwise, <b>FALSE</b>.




## -remarks



Subclass callbacks are identified by the combination of the callback address and the caller-defined subclass ID. If the callback address and ID pair have not yet been installed, then this function installs the subclass. If the pair has already been installed, then this function just updates the reference data.

Each callback can store a single <b>DWORD</b> of reference data, which is passed to the callback function when it is called to filter messages. No reference counting is performed for the callback; it may repeatedly call <b>SetWindowSubclass</b> to alter the value of its reference data element.

<div class="alert"><b>Warning</b>  You cannot use the subclassing helper functions to subclass a window across threads.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb776403(v=VS.85).aspx">DefSubclassProc</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776430(v=VS.85).aspx">GetWindowSubclass</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762094(v=VS.85).aspx">RemoveWindowSubclass</a>
 

 


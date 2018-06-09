---
UID: NF:msime.IFECommon.IsDefaultIME
title: IFECommon::IsDefaultIME
author: windows-sdk-content
description: Determines if the IME specified by the class ID is the default IME on a local computer.
old-location: intl\ifecommon_isdefaultime.htm
old-project: Intl
ms.assetid: FFC3E200-54D4-4C47-A4A3-87AA2A4A2232
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IFECommon interface [Internationalization for Windows Applications],IsDefaultIME method, IFECommon.IsDefaultIME, IFECommon::IsDefaultIME, IsDefaultIME, IsDefaultIME method [Internationalization for Windows Applications], IsDefaultIME method [Internationalization for Windows Applications],IFECommon interface, intl.ifecommon_isdefaultime, msime/IFECommon::IsDefaultIME
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMEUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msime.h
api_name:
 - IFECommon.IsDefaultIME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IFECommon::IsDefaultIME


## -description


Determines if the IME specified by the class ID is the default IME on a local computer.

The name of the IME is obtained from the  <a href="https://msdn.microsoft.com/731b8209-1ca8-4667-bd39-7bd0cef45380">Win32 keyboard layout API</a>.


## -parameters




### -param szName [out]

The name of the IME for the specified class ID. Can be <b>NULL</b>.


### -param cszName [in]

The size of <i>szName</i> in bytes.


## -returns



<ul>
<li><b>S_OK</b> if this Microsoft IME is already the default IME.</li>
<li><b>
S_FALSE</b> if this Microsoft IME is not the default IME.</li>
<li>Otherwise <b>E_FAIL</b>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/9FBECA6F-F162-485D-938F-FADC2D47083E">IFECommon</a>



<a href="https://msdn.microsoft.com/731b8209-1ca8-4667-bd39-7bd0cef45380">Win32 keyboard layout API</a>
 

 


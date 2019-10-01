---
UID: NF:msime.IFECommon.SetDefaultIME
title: IFECommon::SetDefaultIME (msime.h)
author: windows-sdk-content
description: Allows the Microsoft IME to become the default IME in the keyboard layout.
old-location: intl\ifecommon_setdefaultime.htm
tech.root: Intl
ms.assetid: D54AABA7-8FAC-4867-91E7-BAF477F8DAB9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFECommon interface [Internationalization for Windows Applications],SetDefaultIME method, IFECommon.SetDefaultIME, IFECommon::SetDefaultIME, SetDefaultIME, SetDefaultIME method [Internationalization for Windows Applications], SetDefaultIME method [Internationalization for Windows Applications],IFECommon interface, intl.ifecommon_setdefaultime, msime/IFECommon::SetDefaultIME
ms.topic: method
f1_keywords: 
 - "msime/IFECommon.SetDefaultIME"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msime.h
api_name:
 - IFECommon.SetDefaultIME
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFECommon::SetDefaultIME


## -description


Allows the Microsoft IME to become the default IME in the keyboard layout.

This method only applies when Microsoft IME uses the Input Method Manager (IMM) of the operating system.


## -parameters






## -returns



<ul>
<li><b>S_OK</b> if successful.</li>
<li><b>IFEC_S_ALREADY_DEFAULT</b> if this Microsoft IME is already the default IME.</li>
<li>Otherwise <b>E_FAIL</b>.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msime/nn-msime-ifecommon">IFECommon</a>
 

 


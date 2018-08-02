---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerTarget.Unpeg
title: IReferenceTrackerTarget::xaml
author: windows-sdk-content
description: Marks that the reference tracker target is no longer in use by the XAML framework, and can be collected.
old-location: winrt\ireferencetrackertarget_unpeg.htm
old-project: WinRT
ms.assetid: c070957f-3bf8-4e72-ad56-e9cb023692c6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IReferenceTrackerTarget interface [Windows Runtime],Unpeg method, IReferenceTrackerTarget.Unpeg, IReferenceTrackerTarget.xaml, IReferenceTrackerTarget::Unpeg, IReferenceTrackerTarget::xaml, Unpeg, Unpeg method [Windows Runtime], Unpeg method [Windows Runtime],IReferenceTrackerTarget interface, windows/IReferenceTrackerTarget::Unpeg, winrt.ireferencetrackertarget_unpeg
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: windows.ui.xaml.hosting.referencetracker.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.ui.xaml.hosting.referencetracker.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PDF_RENDER_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.ui.xaml.hosting.referencetracker.h
api_name:
 - IReferenceTrackerTarget.Unpeg
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IReferenceTrackerTarget::xaml


## -description


Marks that the reference tracker target is no longer in use by the XAML framework, and can be collected.  


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  You do not need to have parity between calls to <a href="https://msdn.microsoft.com/2750e8b1-eeeb-411a-89a8-b63b26f731ac">Peg</a> and <b>Unpeg</b>. A single call to <b>Unpeg</b> will remove the marker set in all previous calls to <b>Peg</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/204c647d-65c0-4b0e-b0fa-1abe9e8fdedd">IReferenceTrackerTarget</a>
 

 


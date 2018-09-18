---
UID: NF:ctffunc.IUIManagerEventSink.OnWindowUpdating
title: IUIManagerEventSink::OnWindowUpdating
author: windows-sdk-content
description: Called by the TSF before resizing and/or relocating the opened IME UI.
old-location: tsf\iuimanagereventsink_onwindowupdating.htm
tech.root: TSF
ms.assetid: BCCE292C-8A74-4DBA-965D-15249E2EA547
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IUIManagerEventSink interface [Text Services Framework],OnWindowUpdating method, IUIManagerEventSink.OnWindowUpdating, IUIManagerEventSink::OnWindowUpdating, OnWindowUpdating, OnWindowUpdating method [Text Services Framework], OnWindowUpdating method [Text Services Framework],IUIManagerEventSink interface, ctffunc/IUIManagerEventSink::OnWindowUpdating, tsf.iuimanagereventsink_onwindowupdating
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
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
 - Ctffunc.h
api_name:
 - IUIManagerEventSink.OnWindowUpdating
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIManagerEventSink::OnWindowUpdating


## -description


Called by the TSF before resizing and/or relocating the opened IME UI.


## -parameters




### -param prcUpdatedBounds [in]

Pointer to a <b>RECT</b> structure defining the affected area (in screen coordinates). 


## -returns



Ignored.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn495081(v=VS.85).aspx">IUIManagerEventSink</a>
 

 


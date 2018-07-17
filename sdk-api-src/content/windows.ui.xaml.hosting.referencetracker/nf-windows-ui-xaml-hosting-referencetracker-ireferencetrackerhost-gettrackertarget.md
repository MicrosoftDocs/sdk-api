---
UID: NF:windows.ui.xaml.hosting.referencetracker.IReferenceTrackerHost.GetTrackerTarget
title: IReferenceTrackerHost::xaml
author: windows-sdk-content
description: Requests the host to provide a reference tracker target that references a reference tracker source. This tracker target then controls the lifetime of the tracker source.
old-location: winrt\ireferencetrackerhost_gettrackertarget.htm
old-project: WinRT
ms.assetid: 5dabc7ce-a6aa-4acd-b331-3f74b0f2d179
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetTrackerTarget, GetTrackerTarget method [Windows Runtime], GetTrackerTarget method [Windows Runtime],IReferenceTrackerHost interface, IReferenceTrackerHost interface [Windows Runtime],GetTrackerTarget method, IReferenceTrackerHost.GetTrackerTarget, IReferenceTrackerHost.xaml, IReferenceTrackerHost::GetTrackerTarget, IReferenceTrackerHost::xaml, windows/IReferenceTrackerHost::GetTrackerTarget, winrt.ireferencetrackerhost_gettrackertarget
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: windows.ui.xaml.hosting.referencetracker.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
 - IReferenceTrackerHost.GetTrackerTarget
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IReferenceTrackerHost::xaml


## -description


Requests the host to provide a reference tracker target that references a reference tracker source. This tracker target then controls the lifetime of the tracker source.


## -parameters




### -param unknown




### -param newReference






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



  For example, after calling this method, calling <a href="https://msdn.microsoft.com/2750e8b1-eeeb-411a-89a8-b63b26f731ac">Peg</a> on the tracker target will prevent the tracker source from being collected.




## -see-also




<a href="https://msdn.microsoft.com/b17fe8ae-be79-4281-a313-517505017401">IReferenceTrackerHost</a>
 

 


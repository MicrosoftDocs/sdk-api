---
UID: NF:uianimation.IUIAnimationLoopIterationChangeHandler2.OnLoopIterationChanged
title: IUIAnimationLoopIterationChangeHandler2::OnLoopIterationChanged
author: windows-sdk-content
description: Handles loop iteration change events, which occur when a loop within a storyboard begins a new iteration.
old-location: uianimation\iuianimationloopiterationchangehandler2_onloopiterationchanged.htm
tech.root: UIAnimation
ms.assetid: C441CDC6-944E-488A-B643-13A13E027DF6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUIAnimationLoopIterationChangeHandler2 interface [Windows Animation],OnLoopIterationChanged method, IUIAnimationLoopIterationChangeHandler2.OnLoopIterationChanged, IUIAnimationLoopIterationChangeHandler2::OnLoopIterationChanged, OnLoopIterationChanged, OnLoopIterationChanged method [Windows Animation], OnLoopIterationChanged method [Windows Animation],IUIAnimationLoopIterationChangeHandler2 interface, uianimation.iuianimationloopiterationchangehandler2_onloopiterationchanged, uianimation/IUIAnimationLoopIterationChangeHandler2::OnLoopIterationChanged
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAnimation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationLoopIterationChangeHandler2.OnLoopIterationChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationLoopIterationChangeHandler2::OnLoopIterationChanged


## -description


Handles loop iteration change events, which occur when a loop within a storyboard begins a new iteration.


## -parameters




### -param storyboard [in]

The storyboard to which the loop belongs.


### -param id [in]

The loop ID.


### -param newIterationCount [in]

The iteration count for the latest <a href="https://msdn.microsoft.com/5735ABDB-E1AE-41C0-9F37-92084CEF6FAD">IUIAnimationManager2::Update</a>.


### -param oldIterationCount [in]

The iteration count for the previous <a href="https://msdn.microsoft.com/5735ABDB-E1AE-41C0-9F37-92084CEF6FAD">IUIAnimationManager2::Update</a>.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/DB3995BA-856F-407D-AA89-247D84C3F7A1">IUIAnimationLoopIterationChangeHandler2</a>
 

 


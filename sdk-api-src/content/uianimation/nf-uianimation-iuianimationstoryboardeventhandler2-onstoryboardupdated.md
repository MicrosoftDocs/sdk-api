---
UID: NF:uianimation.IUIAnimationStoryboardEventHandler2.OnStoryboardUpdated
title: IUIAnimationStoryboardEventHandler2::OnStoryboardUpdated
author: windows-sdk-content
description: Handles storyboard update events.
old-location: uianimation\iuianimationstoryboardeventhandler2_onstoryboardupdated.htm
tech.root: UIAnimation
ms.assetid: 30AB185A-D555-47CA-A2E6-DAAEB0C56FCD
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIAnimationStoryboardEventHandler2 interface [Windows Animation],OnStoryboardUpdated method, IUIAnimationStoryboardEventHandler2.OnStoryboardUpdated, IUIAnimationStoryboardEventHandler2::OnStoryboardUpdated, OnStoryboardUpdated, OnStoryboardUpdated method [Windows Animation], OnStoryboardUpdated method [Windows Animation],IUIAnimationStoryboardEventHandler2 interface, uianimation.iuianimationstoryboardeventhandler2_onstoryboardupdated, uianimation/IUIAnimationStoryboardEventHandler2::OnStoryboardUpdated
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps \| UWP apps]
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
 - IUIAnimationStoryboardEventHandler2.OnStoryboardUpdated
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationStoryboardEventHandler2::OnStoryboardUpdated


## -description


Handles storyboard update events.


## -parameters




### -param storyboard [in]

The storyboard that has been updated.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method is called when the value of at least one of the variables that a storyboard is animating has changed since the last call to the <a href="https://msdn.microsoft.com/5735ABDB-E1AE-41C0-9F37-92084CEF6FAD">IUIAnimationManager2::Update</a> method.

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>OnStoryboardUpdated</b>:

<ul>
<li>
<a href="https://msdn.microsoft.com/C7B11A34-E5FB-40D7-A655-29D28ECF4068">IUIAnimationManager2::GetStoryboardFromTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ED367DB7-91D6-4D2E-BDAB-27FA4340F091">IUIAnimationManager2::GetVariableFromTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A73D5003-FC28-4A79-B157-3D0D2E0DEB3D">IUIAnimationStoryboard2::GetTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7A9B4A84-94E4-4B6C-B2FF-0A0A70397D21">IUIAnimationVariable2::GetCurrentStoryboard</a>
</li>
<li>
<a href="https://msdn.microsoft.com/290EC1D8-007D-44A0-B3F8-384A9594FDC4">IUIAnimationVariable2::GetFinalIntegerValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/FF39BE67-AED7-4B67-ABAF-D5D51619F0D3">IUIAnimationVariable2::GetFinalValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C878B86A-87AD-457A-802A-9A329B401B08">IUIAnimationVariable2::GetIntegerValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8B25BE8D-B12F-44B4-AFBF-3E6994BA0771">IUIAnimationVariable2::GetPreviousIntegerValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1A2BF7DB-1C7B-43BF-A7F7-A4FB47250597">IUIAnimationVariable2::GetPreviousValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/29E6CA4D-527D-4C9D-9E28-2E2C67516126">IUIAnimationVariable2::GetTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7925D462-C3FD-4BD2-806D-66FE822979EF">IUIAnimationVariable2::GetValue</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/5735ABDB-E1AE-41C0-9F37-92084CEF6FAD">IUIAnimationManager2::Update</a>



<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/901afd34-03cc-4421-a467-9d096e1458fe">IUIAnimationStoryboard2::GetElapsedTime
      </a>



<a href="https://msdn.microsoft.com/2AB8C0C5-2203-4778-BBEA-6D52B727FDDB">IUIAnimationStoryboardEventHandler2</a>
 

 


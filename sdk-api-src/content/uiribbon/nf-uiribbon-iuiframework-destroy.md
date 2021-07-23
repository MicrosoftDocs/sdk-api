---
UID: NF:uiribbon.IUIFramework.Destroy
title: IUIFramework::Destroy (uiribbon.h)
description: Terminates and releases all objects, hooks, and references for an instance of the Windows Ribbon framework.
helpviewer_keywords: ["Destroy","Destroy method [Windows Ribbon]","Destroy method [Windows Ribbon]","IUIFramework interface","IUIFramework interface [Windows Ribbon]","Destroy method","IUIFramework.Destroy","IUIFramework::Destroy","scenicintent_IUIFramework_Destroy","uiribbon/IUIFramework::Destroy","windowsribbon.windowsribbon_iuiframework_destroy"]
old-location: windowsribbon\windowsribbon_iuiframework_destroy.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiframework\destroy.htm
ms.date: 12/05/2018
ms.keywords: Destroy, Destroy method [Windows Ribbon], Destroy method [Windows Ribbon],IUIFramework interface, IUIFramework interface [Windows Ribbon],Destroy method, IUIFramework.Destroy, IUIFramework::Destroy, scenicintent_IUIFramework_Destroy, uiribbon/IUIFramework::Destroy, windowsribbon.windowsribbon_iuiframework_destroy
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mshtml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
ms.custom: 19H1
f1_keywords:
 - IUIFramework::Destroy
 - uiribbon/IUIFramework::Destroy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUIFramework.Destroy
---

# IUIFramework::Destroy


## -description

Terminates and releases all objects, hooks, and references for an instance of the Windows Ribbon framework.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method must be called once for each instance of <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework">IUIFramework</a>.
			

If  <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize">IUIFramework::Initialize</a> was called, then <b>IUIFramework::Destroy</b> must be called to free resources and ensure proper dismantling of the framework. Failure to call <b>IUIFramework::Destroy</b> may cause a memory leak.

## -see-also

<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework">IUIFramework</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>

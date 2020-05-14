---
UID: NF:corewindow.CreateControlInput
title: CreateControlInput function (corewindow.h)
description: Creates a ICoreInputSourceBase object in the caller’s UI thread.helpviewer_keywords: ["CreateControlInput","CreateControlInput function [Windows Runtime]","corewindow/CreateControlInput","winrt.createcontrolinput"]
old-location: winrt\createcontrolinput.htm
tech.root: WinRT
ms.assetid: 562F6745-DE20-43A9-8A40-A98F478DD505
ms.date: 12/05/2018
ms.keywords: CreateControlInput, CreateControlInput function [Windows Runtime], corewindow/CreateControlInput, winrt.createcontrolinput
f1_keywords:
- corewindow/CreateControlInput
dev_langs:
- c++
req.header: corewindow.h
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
req.dll: Windows.UI.Core.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Windows.UI.Core.dll
api_name:
- CreateControlInput
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateControlInput function


## -description


Creates a <a href="https://docs.microsoft.com/uwp/api/windows.ui.core.icoreinputsourcebase">ICoreInputSourceBase</a> object in the caller’s UI thread.


## -parameters




### -param riid [in]

Interface ID of the object. Must to be set to the UUID for  <a href="https://docs.microsoft.com/uwp/api/windows.ui.core.icoreinputsourcebase">ICoreInputSourceBase</a>, which is 9F488807-4580-4BE8-BE68-92A9311713BB.


### -param ppv [out]

Pointer to receive the <a href="https://docs.microsoft.com/uwp/api/windows.ui.core.icoreinputsourcebase">ICoreInputSourceBase</a> object.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This API must be called from the UI thread to create <a href="https://docs.microsoft.com/uwp/api/windows.ui.core.icoreinputsourcebase">ICoreInputSourceBase</a> object. The object created using this API can be used only in that thread in which it was created. 

If the call is successful, the  caller can call <b>QueryInterface</b> on the returned <a href="https://docs.microsoft.com/uwp/api/windows.ui.core.icoreinputsourcebase">ICoreInputSourceBase</a> object to obtain the <a href="https://docs.microsoft.com/windows/desktop/api/corewindow/nn-corewindow-icoreinputinterop">ICoreInputInterop</a> object that created it.




## -see-also




<a href="https://docs.microsoft.com/uwp/api/windows.ui.core.icoreinputsourcebase">ICoreInputSourceBase</a>
 

 


---
UID: NF:corewindow.CreateControlInputEx
title: CreateControlInputEx function (corewindow.h)
description: Creates a ICoreInputSourceBase object in a worker thread or the UI thread.helpviewer_keywords: ["CreateControlInputEx","CreateControlInputEx function [Windows Runtime]","corewindow/CreateControlInputEx","winrt.createcontrolinputex"]
old-location: winrt\createcontrolinputex.htm
tech.root: WinRT
ms.assetid: AF12DA9F-7E5A-43B0-8B4D-7E41C4C1361F
ms.date: 12/05/2018
ms.keywords: CreateControlInputEx, CreateControlInputEx function [Windows Runtime], corewindow/CreateControlInputEx, winrt.createcontrolinputex
f1_keywords:
- corewindow/CreateControlInputEx
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
req.dll: Windows.UI.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Windows.UI.dll
api_name:
- CreateControlInputEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateControlInputEx function


## -description


Creates a <a href="https://docs.microsoft.com/uwp/api/windows.ui.core.icoreinputsourcebase">ICoreInputSourceBase</a> object in a worker thread or the UI thread. 


## -parameters




### -param pCoreWindow [in]

Pointer to the parent <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> to which the <a href="https://docs.microsoft.com/uwp/api/windows.ui.core.icoreinputsourcebase">ICoreInputSourceBase</a> object will be attached. This parameter can’t be NULL.


### -param riid [in]

Interface ID of the object. Must to be set to the UUID for  <a href="https://docs.microsoft.com/uwp/api/windows.ui.core.icoreinputsourcebase">ICoreInputSourceBase</a>, which is 9F488807-4580-4BE8-BE68-92A9311713BB.


### -param ppv [out]

Pointer to receive the <a href="https://docs.microsoft.com/uwp/api/windows.ui.core.icoreinputsourcebase">ICoreInputSourceBase</a> object.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This API must be called from the UI thread or worker thread to create <a href="https://docs.microsoft.com/uwp/api/windows.ui.core.icoreinputsourcebase">ICoreInputSourceBase</a> object. The object created using this API can be used only in that thread in which it was created. 

If the call is successful, the  caller can call <b>QueryInterface</b> on the returned <a href="https://docs.microsoft.com/uwp/api/windows.ui.core.icoreinputsourcebase">ICoreInputSourceBase</a> object to obtain the <a href="https://docs.microsoft.com/windows/desktop/api/corewindow/nn-corewindow-icoreinputinterop">ICoreInputInterop</a> object that created it.

This API will fail if the following scenarios occur:

<ul>
<li>The <i>pCoreWindow</i> parameter is <b>NULL</b>.</li>
<li>If the <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> passed is not same as the <b>CoreWindow</b> present in the calling thread. </li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/uwp/api/windows.ui.core.icoreinputsourcebase">ICoreInputSourceBase</a>
 

 


---
UID: NF:corewindow.CreateControlInput
title: CreateControlInput function
author: windows-sdk-content
description: Creates a ICoreInputSourceBase object in the caller’s UI thread.
old-location: winrt\createcontrolinput.htm
old-project: WinRT
ms.assetid: 562F6745-DE20-43A9-8A40-A98F478DD505
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateControlInput, CreateControlInput function [Windows Runtime], corewindow/CreateControlInput, winrt.createcontrolinput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: corewindow.h
req.include-header: 
req.redist: 
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
req.typenames: WMPContextMenuInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windows.UI.Core.dll
api_name:
 - CreateControlInput
product: Windows
targetos: Windows
req.lib: 
req.dll: Windows.UI.Core.dll
req.irql: 
---

# CreateControlInput function


## -description


Creates a <a href="https://msdn.microsoft.com/675ca745-c593-4714-9fae-5fcab2c0336e">ICoreInputSourceBase</a> object in the caller’s UI thread.


## -parameters




### -param riid [in]

Interface ID of the object. Must to be set to the UUID for  <a href="https://msdn.microsoft.com/675ca745-c593-4714-9fae-5fcab2c0336e">ICoreInputSourceBase</a>, which is 9F488807-4580-4BE8-BE68-92A9311713BB.


### -param ppv [out]

Pointer to receive the <a href="https://msdn.microsoft.com/675ca745-c593-4714-9fae-5fcab2c0336e">ICoreInputSourceBase</a> object.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This API must be called from the UI thread to create <a href="https://msdn.microsoft.com/675ca745-c593-4714-9fae-5fcab2c0336e">ICoreInputSourceBase</a> object. The object created using this API can be used only in that thread in which it was created. 

If the call is successful, the  caller can call <b>QueryInterface</b> on the returned <a href="https://msdn.microsoft.com/675ca745-c593-4714-9fae-5fcab2c0336e">ICoreInputSourceBase</a> object to obtain the <a href="https://msdn.microsoft.com/en-us/library/Dn302114(v=VS.85).aspx">ICoreInputInterop</a> object that created it.




## -see-also




<a href="https://msdn.microsoft.com/675ca745-c593-4714-9fae-5fcab2c0336e">ICoreInputSourceBase</a>
 

 


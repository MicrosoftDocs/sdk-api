---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMultipleViewProvider::GetViewName


## -description


Retrieves the name of a control-specific view.


## -parameters




### -param viewId [in]

Type: <b>int</b>

A view identifier.


### -param pRetVal [out, retval]

Type: <b>BSTR*</b>

Receives a localized name for the view. 
                This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            View identifiers can be retrieved by using <a href="https://msdn.microsoft.com/fd4d5616-c126-455e-84e7-e62e24daf8f9">IMultipleViewProvider::GetSupportedViews</a>.
            


            The collection of view identifiers must be identical for all instances of a control.
            


            View names must be suitable for use in text-to-speech, Braille, and other accessible applications.
            




## -see-also




<a href="https://msdn.microsoft.com/84d370a6-05bd-4efb-a6ca-99e9392f95dc">IMultipleViewProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 


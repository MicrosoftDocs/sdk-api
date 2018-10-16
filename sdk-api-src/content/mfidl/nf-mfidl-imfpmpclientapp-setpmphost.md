---
UID: NF:mfidl.IMFPMPClientApp.SetPMPHost
title: IMFPMPClientApp::SetPMPHost
author: windows-sdk-content
description: Sets a pointer to the IMFPMPHostApp interface allowing a media source to create objects in the PMP process.
old-location: mf\imfpmpclientapp_setpmphost.htm
tech.root: medfound
ms.assetid: 8809e691-f0cf-4c1f-8409-5e7fbac46b16
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IMFPMPClientApp interface [Media Foundation],SetPMPHost method, IMFPMPClientApp.SetPMPHost, IMFPMPClientApp::SetPMPHost, SetPMPHost, SetPMPHost method [Media Foundation], SetPMPHost method [Media Foundation],IMFPMPClientApp interface, mf.imfpmpclientapp_setpmphost, mfidl/IMFPMPClientApp::SetPMPHost
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
 - Mfidl.idl
api_name:
 - IMFPMPClientApp.SetPMPHost
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMPClientApp::SetPMPHost


## -description


Sets a pointer to the <a href="https://msdn.microsoft.com/ca24930d-bd1e-4c12-8246-1e505a98944a">IMFPMPHostApp</a> interface allowing a media source to create objects in the PMP process.


## -parameters




### -param pPMPHost [in]

A pointer to the <a href="https://msdn.microsoft.com/ca24930d-bd1e-4c12-8246-1e505a98944a">IMFPMPHostApp</a> interface.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/03cd9e3c-65ac-40ad-802d-e36127dbd61f">IMFPMPClientApp</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/CF3A427D-31D2-45FF-BE87-F192B758204E">PMP Media Session</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 


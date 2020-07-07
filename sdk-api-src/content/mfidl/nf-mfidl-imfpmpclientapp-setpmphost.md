---
UID: NF:mfidl.IMFPMPClientApp.SetPMPHost
title: IMFPMPClientApp::SetPMPHost (mfidl.h)
description: Sets a pointer to the IMFPMPHostApp interface allowing a media source to create objects in the PMP process.
helpviewer_keywords: ["IMFPMPClientApp interface [Media Foundation]","SetPMPHost method","IMFPMPClientApp.SetPMPHost","IMFPMPClientApp::SetPMPHost","SetPMPHost","SetPMPHost method [Media Foundation]","SetPMPHost method [Media Foundation]","IMFPMPClientApp interface","mf.imfpmpclientapp_setpmphost","mfidl/IMFPMPClientApp::SetPMPHost"]
old-location: mf\imfpmpclientapp_setpmphost.htm
tech.root: medfound
ms.assetid: 8809e691-f0cf-4c1f-8409-5e7fbac46b16
ms.date: 12/05/2018
ms.keywords: IMFPMPClientApp interface [Media Foundation],SetPMPHost method, IMFPMPClientApp.SetPMPHost, IMFPMPClientApp::SetPMPHost, SetPMPHost, SetPMPHost method [Media Foundation], SetPMPHost method [Media Foundation],IMFPMPClientApp interface, mf.imfpmpclientapp_setpmphost, mfidl/IMFPMPClientApp::SetPMPHost
f1_keywords:
- mfidl/IMFPMPClientApp.SetPMPHost
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMPClientApp::SetPMPHost


## -description


Sets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpmphostapp">IMFPMPHostApp</a> interface allowing a media source to create objects in the PMP process.


## -parameters




### -param pPMPHost [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpmphostapp">IMFPMPHostApp</a> interface.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpmpclientapp">IMFPMPClientApp</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/pmp-media-session">PMP Media Session</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/protected-media-path">Protected Media Path</a>
 

 


---
UID: NF:mfidl.IMFPMPClient.SetPMPHost
title: IMFPMPClient::SetPMPHost (mfidl.h)
description: Provides a pointer to the IMFPMPHost interface.helpviewer_keywords: ["IMFPMPClient interface [Media Foundation]","SetPMPHost method","IMFPMPClient.SetPMPHost","IMFPMPClient::SetPMPHost","SetPMPHost","SetPMPHost method [Media Foundation]","SetPMPHost method [Media Foundation]","IMFPMPClient interface","d6e48f36-7896-4e6d-ba10-d8c0288ccffc","mf.imfpmpclient_setpmphost","mfidl/IMFPMPClient::SetPMPHost"]
old-location: mf\imfpmpclient_setpmphost.htm
tech.root: medfound
ms.assetid: d6e48f36-7896-4e6d-ba10-d8c0288ccffc
ms.date: 12/05/2018
ms.keywords: IMFPMPClient interface [Media Foundation],SetPMPHost method, IMFPMPClient.SetPMPHost, IMFPMPClient::SetPMPHost, SetPMPHost, SetPMPHost method [Media Foundation], SetPMPHost method [Media Foundation],IMFPMPClient interface, d6e48f36-7896-4e6d-ba10-d8c0288ccffc, mf.imfpmpclient_setpmphost, mfidl/IMFPMPClient::SetPMPHost
f1_keywords:
- mfidl/IMFPMPClient.SetPMPHost
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFPMPClient.SetPMPHost
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMPClient::SetPMPHost


## -description


Provides a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpmphost">IMFPMPHost</a> interface.
        


## -parameters




### -param pPMPHost [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpmphost">IMFPMPHost</a> interface.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpmphost">IMFPMPHost</a> pointer is apartment threaded. The media source must add the pointer to the global interface table (GIT) before using it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient">IMFPMPClient</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/pmp-media-session">PMP Media Session</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/protected-media-path">Protected Media Path</a>
 

 


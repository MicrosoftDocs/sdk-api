---
UID: NF:mfidl.IMFPMPClient.SetPMPHost
title: IMFPMPClient::SetPMPHost
author: windows-sdk-content
description: Provides a pointer to the IMFPMPHost interface.
old-location: mf\imfpmpclient_setpmphost.htm
old-project: medfound
ms.assetid: d6e48f36-7896-4e6d-ba10-d8c0288ccffc
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFPMPClient interface [Media Foundation],SetPMPHost method, IMFPMPClient.SetPMPHost, IMFPMPClient::SetPMPHost, SetPMPHost, SetPMPHost method [Media Foundation], SetPMPHost method [Media Foundation],IMFPMPClient interface, d6e48f36-7896-4e6d-ba10-d8c0288ccffc, mf.imfpmpclient_setpmphost, mfidl/IMFPMPClient::SetPMPHost
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MFSensorDeviceMode
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
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMPClient::SetPMPHost


## -description


Provides a pointer to the <a href="https://msdn.microsoft.com/fab1fb42-07c5-4a74-b6f5-0950b2c3ba46">IMFPMPHost</a> interface.
        


## -parameters




### -param pPMPHost [in]

A pointer to the <a href="https://msdn.microsoft.com/fab1fb42-07c5-4a74-b6f5-0950b2c3ba46">IMFPMPHost</a> interface.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/fab1fb42-07c5-4a74-b6f5-0950b2c3ba46">IMFPMPHost</a> pointer is apartment threaded. The media source must add the pointer to the global interface table (GIT) before using it.




## -see-also




<a href="https://msdn.microsoft.com/adfba5dd-eae6-48f3-a155-65bd491c952c">IMFPMPClient</a>



<a href="https://msdn.microsoft.com/CF3A427D-31D2-45FF-BE87-F192B758204E">PMP Media Session</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 


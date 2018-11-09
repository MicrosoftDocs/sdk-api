---
UID: NF:d3d11.ID3D11VideoContext.FinishSessionKeyRefresh
title: ID3D11VideoContext::FinishSessionKeyRefresh
author: windows-sdk-content
description: Switches to a new session key.
old-location: mf\id3d11videocontext_finishsessionkeyrefresh.htm
tech.root: medfound
ms.assetid: 2F602A5E-B5D1-4749-8696-9F0594770B4F
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: FinishSessionKeyRefresh, FinishSessionKeyRefresh method [Media Foundation], FinishSessionKeyRefresh method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],FinishSessionKeyRefresh method, ID3D11VideoContext.FinishSessionKeyRefresh, ID3D11VideoContext::FinishSessionKeyRefresh, d3d11/ID3D11VideoContext::FinishSessionKeyRefresh, mf.id3d11videocontext_finishsessionkeyrefresh
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
 - d3d11.h
api_name:
 - ID3D11VideoContext.FinishSessionKeyRefresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::FinishSessionKeyRefresh


## -description


Switches to a new session key.




## -parameters




### -param pCryptoSession [in]

A pointer to the <a href="https://msdn.microsoft.com/E17F39CB-61E3-44EF-805D-AD386743744E">ID3D11CryptoSession</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function can only be called when the <a href="https://msdn.microsoft.com/19697660-DDB8-4A4C-888F-018BC5CCFC94">D3D11_CONTENT_PROTECTION_CAPS_FRESHEN_SESSION_KEY</a> cap is reported.

Before calling this method, call <a href="https://msdn.microsoft.com/63376BFE-BA84-4268-8AA8-128BEB83AE78">ID3D11VideoContext::StartSessionKeyRefresh</a>. The <b>StartSessionKeyRefresh</b> method gets a random number from the driver, which is used to create a new session key. The new session key does not become active until the application calls <b>FinishSessionKeyRefresh</b>. After the application calls <b>FinishSessionKeyRefresh</b>, all protected surfaces are encrypted using the new session key.






## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 


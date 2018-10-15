---
UID: NF:d3d9.IDirect3DCryptoSession9.FinishSessionKeyRefresh
title: IDirect3DCryptoSession9::FinishSessionKeyRefresh
author: windows-sdk-content
description: Switches to a new session key.
old-location: mf\idirect3dcryptosession9_finishsessionkeyrefresh.htm
tech.root: medfound
ms.assetid: b5e4522b-d5a5-4ece-9b78-2cebdf9f9364
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: FinishSessionKeyRefresh, FinishSessionKeyRefresh method [Media Foundation], FinishSessionKeyRefresh method [Media Foundation],IDirect3DCryptoSession9 interface, IDirect3DCryptoSession9 interface [Media Foundation],FinishSessionKeyRefresh method, IDirect3DCryptoSession9.FinishSessionKeyRefresh, IDirect3DCryptoSession9::FinishSessionKeyRefresh, d3d9/IDirect3DCryptoSession9::FinishSessionKeyRefresh, mf.idirect3dcryptosession9_finishsessionkeyrefresh
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - d3d9.h
api_name:
 - IDirect3DCryptoSession9.FinishSessionKeyRefresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DCryptoSession9::FinishSessionKeyRefresh


## -description


Switches to a new session key.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before calling this method, call the <a href="https://msdn.microsoft.com/f25ad491-9ffb-40d1-94c3-af0cbae553bf">IDirect3DCryptoSession9::StartSessionKeyRefresh</a> method. The <b>StartSessionKeyRefresh</b> method gets a random number from the driver, which is used to create a new session key. The new session key does not become active until the application calls  <b>FinishSessionKeyRefresh</b>. After the application calls <b>FinishSessionKeyRefresh</b>, all protected surfaces are encrypted using the new session key.




## -see-also




<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>



<a href="https://msdn.microsoft.com/2511c9da-e696-4e49-b180-7fc1317c1652">IDirect3DCryptoSession9</a>
 

 


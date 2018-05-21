---
UID: NF:d3d9.IDirect3DCryptoSession9.StartSessionKeyRefresh
title: IDirect3DCryptoSession9::StartSessionKeyRefresh
author: windows-driver-content
description: Gets a random number that can be used to refresh the session key.
old-location: mf\idirect3dcryptosession9_startsessionkeyrefresh.htm
old-project: medfound
ms.assetid: f25ad491-9ffb-40d1-94c3-af0cbae553bf
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IDirect3DCryptoSession9 interface [Media Foundation],StartSessionKeyRefresh method, IDirect3DCryptoSession9.StartSessionKeyRefresh, IDirect3DCryptoSession9::StartSessionKeyRefresh, StartSessionKeyRefresh, StartSessionKeyRefresh method [Media Foundation], StartSessionKeyRefresh method [Media Foundation],IDirect3DCryptoSession9 interface, d3d9/IDirect3DCryptoSession9::StartSessionKeyRefresh, mf.idirect3dcryptosession9_startsessionkeyrefresh
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d9.h
api_name:
-	IDirect3DCryptoSession9.StartSessionKeyRefresh
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirect3DCryptoSession9::StartSessionKeyRefresh


## -description


Gets a random number that can be used to refresh the session key.


## -parameters




### -param pRandomNumber

A pointer to a byte array that receives a random number.


### -param RandomNumberSize

The size of the <i>pRandomNumber</i> array, in bytes. The size should match the size of the session key.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To generate a new session key, perform a bitwise <b>XOR</b> between the previous session key and the random number. The new session key does not take affect until the application calls <a href="https://msdn.microsoft.com/b5e4522b-d5a5-4ece-9b78-2cebdf9f9364">IDirect3DCryptoSession9::FinishSessionKeyRefresh</a>.

If the driver supports this method, the driver sets the <b>D3DCPCAPS_FRESHENSESSIONKEY</b>
capabilities flag in  the <a href="https://msdn.microsoft.com/4093e64c-340d-4f66-97ed-45bae3b259eb">IDirect3DDevice9Video::GetContentProtectionCaps</a> method.




## -see-also




<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>



<a href="https://msdn.microsoft.com/2511c9da-e696-4e49-b180-7fc1317c1652">IDirect3DCryptoSession9</a>
 

 


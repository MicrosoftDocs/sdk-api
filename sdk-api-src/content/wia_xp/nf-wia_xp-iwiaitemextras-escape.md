---
UID: NF:wia_xp.IWiaItemExtras.Escape
title: IWiaItemExtras::Escape method
author: windows-driver-content
description: The IWiaItemExtras::Escape method sends a request for a vendor-specific I/O operation to a still image device.
old-location: wia\_wia_IWiaItemExtras_Escape.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitemextras\escape.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: Escape method [WIA], Escape method [WIA], IWiaItemExtras interface, Escape,IWiaItemExtras.Escape, IWiaItemExtras, IWiaItemExtras interface [WIA], Escape method, IWiaItemExtras::Escape, _wia_IWiaItemExtras_Escape, wia._wia_IWiaItemExtras_Escape, wia_xp/IWiaItemExtras::Escape
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wiaservc.dll
api_name:
-	IWiaItemExtras.Escape
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaItemExtras::Escape method


## -description


The <b>IWiaItemExtras::Escape</b> method sends a request for a vendor-specific I/O operation to a still image device.


## -parameters




### -param dwEscapeCode [in]

Type: <b>DWORD</b>

Calling application-supplied, vendor-defined, DWORD-sized value that represents an I/O operation.


### -param lpInData [in]

Type: <b>BYTE*</b>

Pointer to a calling application-supplied buffer that contains data to be sent to the device.


### -param cbInDataSize [in]

Type: <b>DWORD</b>

Calling application-supplied length, in bytes, of the data contained in the buffer pointed to by <i>lpInData</i>.


### -param pOutData [out]

Type: <b>BYTE*</b>

Pointer to a calling application-supplied memory buffer to receive data from the device.


### -param dwOutDataSize [in]

Type: <b>DWORD</b>

Calling application-supplied length, in bytes, of the buffer pointed to by <i>pOutData</i>.


### -param pdwActualDataSize [out]

Type: <b>DWORD*</b>

Receives the number of bytes actually written to <i>pOutData</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b04f22dc-47d2-4434-82f9-4d6c618f31b3">IWiaItemExtras</a>
 

 


---
UID: NF:encdec.IXDSCodecConfig.GetSecureChannelObject
title: IXDSCodecConfig::GetSecureChannelObject
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\ixdscodecconfig_getsecurechannelobject.htm
tech.root: MSTV
ms.assetid: c7bf4efe-110a-4bcc-927c-f5e4798211df
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetSecureChannelObject, GetSecureChannelObject method [Microsoft TV Technologies], GetSecureChannelObject method [Microsoft TV Technologies],IXDSCodecConfig interface, IXDSCodecConfig interface [Microsoft TV Technologies],GetSecureChannelObject method, IXDSCodecConfig.GetSecureChannelObject, IXDSCodecConfig::GetSecureChannelObject, IXDSCodecConfigGetSecureChannelObject, encdec/IXDSCodecConfig::GetSecureChannelObject, mstv.ixdscodecconfig_getsecurechannelobject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: encdec.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EncDec.h
api_name:
 - IXDSCodecConfig.GetSecureChannelObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- encdec.h
: 
- IXDSCodecConfig.GetSecureChannelObject
: 
---

# IXDSCodecConfig::GetSecureChannelObject


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>GetSecureChannelObject</b> method retrieves the secure channel object used to decrypt the stream.


## -parameters




### -param ppUnkDRMSecureChannel [out]

Receives a pointer to the secure channel object's <b>IUnknown</b> interface.


## -returns



Returns an <b>HRESULT</b>.




## -remarks



If the method succeeds, the caller must release the <b>IUnknown</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/90f8ce9b-2a85-43d0-9f2a-a3d248414a2d">IXDSCodecConfig Interface</a>
 

 


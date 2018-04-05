---
UID: NF:dxva.IDirect3DDXVADevice9.Execute
title: IDirect3DDXVADevice9::Execute method
author: windows-driver-content
description: Performs a DirectX Video Acceleration (DXVA) decoding operation.
old-location: mf\idirect3ddxvadevice9_execute.htm
old-project: medfound
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: Execute method [Media Foundation], Execute method [Media Foundation], IDirect3DDXVADevice9 interface, Execute,IDirect3DDXVADevice9.Execute, IDirect3DDXVADevice9, IDirect3DDXVADevice9 interface [Media Foundation], Execute method, IDirect3DDXVADevice9::Execute, dxva/IDirect3DDXVADevice9::Execute, mf.idirect3ddxvadevice9_execute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxva.h
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
req.typenames: COPP_TVProtectionStandard
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxva.h
api_name:
-	IDirect3DDXVADevice9.Execute
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirect3DDXVADevice9::Execute method


## -description


Performs a DirectX Video Acceleration (DXVA) decoding operation.
      


## -parameters




### -param FunctionNum

A <b>DWORD</b> that contains one or more DXVA function numbers. For details, refer to the <a href="http://go.microsoft.com/fwlink/p/?linkid=93647">DXVA 1.0 specification</a>.


### -param pInputData


            A pointer to a buffer that contains input data for the decoding operation. The meaning of this data depends on the surface type and function number.


### -param InputSize

The size of the input data, in bytes.


### -param OuputData




### -param OutputSize

The size of the <i>OutputData</i> buffer, in bytes.


### -param NumBuffers

The number of elements in the <i>pBufferInfo</i> array.
          


### -param pBufferInfo

A pointer to an array of <a href="https://msdn.microsoft.com/048a3fcf-6076-4500-b5cc-edfe782f467b">DXVABufferInfo</a> structures.


#### - OutputData

Pointer to a buffer where the video accelerator writes output data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/63f77cf9-4c04-4ddb-9582-cfcf86f66a2a">IDirect3DDXVADevice9</a>
 

 


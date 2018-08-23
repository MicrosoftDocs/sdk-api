---
UID: NF:d2d1_3.ID2D1Device3.CreateDeviceContext
title: ID2D1Device3::CreateDeviceContext
author: windows-sdk-content
description: Creates a new ID2D1DeviceContext3 from this Direct2D device.
old-location: direct2d\id2d1device3_createdevicecontext.htm
old-project: direct2d
ms.assetid: DA82C681-7A9B-42A4-AC02-CD8ACFDB7F0E
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateDeviceContext, CreateDeviceContext method [Direct2D], CreateDeviceContext method [Direct2D],ID2D1Device3 interface, ID2D1Device3 interface [Direct2D],CreateDeviceContext method, ID2D1Device3.CreateDeviceContext, ID2D1Device3::CreateDeviceContext, d2d1_3/ID2D1Device3::CreateDeviceContext, direct2d.id2d1device3_createdevicecontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d2d1_3.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Device3.CreateDeviceContext
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# ID2D1Device3::CreateDeviceContext


## -description


Creates a new <a href="https://msdn.microsoft.com/AD763619-7880-41EB-8446-2E4B84CB4EAC">ID2D1DeviceContext3</a> from this Direct2D device.


## -parameters




### -param options

Type: <b><a href="https://msdn.microsoft.com/be4e6eb7-0767-4faf-9f27-eeb3bed48244">D2D1_DEVICE_CONTEXT_OPTIONS</a></b>

The options to be applied to the created device context.


### -param deviceContext3 [out]

Type: <b><a href="https://msdn.microsoft.com/AD763619-7880-41EB-8446-2E4B84CB4EAC">ID2D1DeviceContext3</a>**</b>

When this method returns, contains a pointer to the new device context.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/60CB6308-85BE-424B-9950-1C8617D08A09">ID2D1Device3</a>
 

 


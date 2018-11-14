---
UID: NF:mfmediaengine.IMFMediaEngineExtension.CancelObjectCreation
title: IMFMediaEngineExtension::CancelObjectCreation
author: windows-sdk-content
description: Cancels the current request to create an object.
old-location: mf\imfmediaengineextension_cancelobjectcreation.htm
tech.root: medfound
ms.assetid: E2FEC865-221E-41B5-8271-32A53D60619E
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CancelObjectCreation, CancelObjectCreation method [Media Foundation], CancelObjectCreation method [Media Foundation],IMFMediaEngineExtension interface, IMFMediaEngineExtension interface [Media Foundation],CancelObjectCreation method, IMFMediaEngineExtension.CancelObjectCreation, IMFMediaEngineExtension::CancelObjectCreation, mf.imfmediaengineextension_cancelobjectcreation, mfmediaengine/IMFMediaEngineExtension::CancelObjectCreation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
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
 - mfmediaengine.h
api_name:
 - IMFMediaEngineExtension.CancelObjectCreation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfmediaengine.h
: 
- IMFMediaEngineExtension.CancelObjectCreation
: 
---

# IMFMediaEngineExtension::CancelObjectCreation


## -description


Cancels the current request to create an object.


## -parameters




### -param pIUnknownCancelCookie [in]

The pointer that was returned in the the <i>ppIUnknownCancelCookie</i> parameter of the <a href="https://msdn.microsoft.com/804E9F16-E4C9-41F6-8913-950A569FB835">IMFMediaEngineExtension::BeginCreateObject</a> method.




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method attempts to cancel a previous call to <a href="https://msdn.microsoft.com/804E9F16-E4C9-41F6-8913-950A569FB835">BeginCreateObject</a>. Because that method is asynchronous, however, it might complete before the operation can be canceled.




## -see-also




<a href="https://msdn.microsoft.com/A032E0D0-2201-4B81-9FE0-8E9CE2707FDB">IMFMediaEngineExtension</a>
 

 


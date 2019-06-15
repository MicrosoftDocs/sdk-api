---
UID: NF:mfidl.MFCreatePropertiesFromMediaType
title: MFCreatePropertiesFromMediaType function (mfidl.h)
author: windows-sdk-content
description: Creates properties from a IMFMediaType.
old-location: mf\mfcreatepropertiesfrommediatype.htm
tech.root: medfound
ms.assetid: D9B639BB-285C-40BF-B111-2C5501E41CE1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFCreatePropertiesFromMediaType, MFCreatePropertiesFromMediaType function [Media Foundation], mf.mfcreatepropertiesfrommediatype, mfidl/MFCreatePropertiesFromMediaType
ms.topic: function
req.header: mfidl.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreatePropertiesFromMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreatePropertiesFromMediaType function


## -description


Creates properties from a <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>.


## -parameters




### -param pMediaType [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface.


### -param riid [in]

The interface identifier (IID) of the interface being requested. 


### -param ppv [out]

Receives a pointer to the requested interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 


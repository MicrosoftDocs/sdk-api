---
UID: NF:mfapi.MFCreateMediaType
title: MFCreateMediaType function
author: windows-sdk-content
description: Creates an empty media type.
old-location: mf\mfcreatemediatype.htm
tech.root: medfound
ms.assetid: 05b0941e-03ce-4ced-9022-22b65d1c4b4c
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: 05b0941e-03ce-4ced-9022-22b65d1c4b4c, MFCreateMediaType, MFCreateMediaType function [Media Foundation], mf.mfcreatemediatype, mfapi/MFCreateMediaType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - MFCreateMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateMediaType function


## -description



Creates an empty media type.




## -parameters




### -param ppMFType

Receives a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The media type is created without any attributes.
      




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 


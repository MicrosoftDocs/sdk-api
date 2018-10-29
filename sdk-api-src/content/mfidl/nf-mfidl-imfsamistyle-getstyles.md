---
UID: NF:mfidl.IMFSAMIStyle.GetStyles
title: IMFSAMIStyle::GetStyles
author: windows-sdk-content
description: Gets a list of the style names defined in the SAMI file.
old-location: mf\imfsamistyle_getstyles.htm
tech.root: medfound
ms.assetid: e0b183f0-8781-4fc5-97dd-e42b0e7bd5e5
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetStyles, GetStyles method [Media Foundation], GetStyles method [Media Foundation],IMFSAMIStyle interface, IMFSAMIStyle interface [Media Foundation],GetStyles method, IMFSAMIStyle.GetStyles, IMFSAMIStyle::GetStyles, e0b183f0-8781-4fc5-97dd-e42b0e7bd5e5, mf.imfsamistyle_getstyles, mfidl/IMFSAMIStyle::GetStyles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSAMIStyle.GetStyles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSAMIStyle::GetStyles


## -description


Gets a list of the style names defined in the SAMI file.
        


## -parameters




### -param pPropVarStyleArray [out]

Pointer to a <b>PROPVARIANT</b> that receives an array of null-terminated wide-character strings. The <b>PROPVARIANT</b> type is VT_VECTOR | VT_LPWSTR. The caller must clear the <b>PROPVARIANT</b> by calling <b>PropVariantClear</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c4887c52-57af-4783-b853-11fe6ad3510e">IMFSAMIStyle</a>



<a href="https://msdn.microsoft.com/007c8181-089e-4e56-a31d-9d1942f90b07">SAMI Media Source</a>
 

 


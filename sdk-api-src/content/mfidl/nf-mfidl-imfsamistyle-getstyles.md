---
UID: NF:mfidl.IMFSAMIStyle.GetStyles
title: IMFSAMIStyle::GetStyles method
author: windows-driver-content
description: Gets a list of the style names defined in the SAMI file.
old-location: mf\imfsamistyle_getstyles.htm
old-project: medfound
ms.assetid: e0b183f0-8781-4fc5-97dd-e42b0e7bd5e5
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: GetStyles method [Media Foundation], GetStyles method [Media Foundation], IMFSAMIStyle interface, GetStyles,IMFSAMIStyle.GetStyles, IMFSAMIStyle, IMFSAMIStyle interface [Media Foundation], GetStyles method, IMFSAMIStyle::GetStyles, e0b183f0-8781-4fc5-97dd-e42b0e7bd5e5, mf.imfsamistyle_getstyles, mfidl/IMFSAMIStyle::GetStyles
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFSAMIStyle.GetStyles
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSAMIStyle::GetStyles method


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
 

 


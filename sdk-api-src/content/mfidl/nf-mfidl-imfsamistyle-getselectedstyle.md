---
UID: NF:mfidl.IMFSAMIStyle.GetSelectedStyle
title: IMFSAMIStyle::GetSelectedStyle method
author: windows-driver-content
description: Gets the current style from the SAMI media source.
old-location: mf\imfsamistyle_getselectedstyle.htm
old-project: medfound
ms.assetid: 7501a4d5-eb5f-4f62-ae55-96ee999e561c
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 7501a4d5-eb5f-4f62-ae55-96ee999e561c, GetSelectedStyle method [Media Foundation], GetSelectedStyle method [Media Foundation], IMFSAMIStyle interface, GetSelectedStyle,IMFSAMIStyle.GetSelectedStyle, IMFSAMIStyle, IMFSAMIStyle interface [Media Foundation], GetSelectedStyle method, IMFSAMIStyle::GetSelectedStyle, mf.imfsamistyle_getselectedstyle, mfidl/IMFSAMIStyle::GetSelectedStyle
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
-	IMFSAMIStyle.GetSelectedStyle
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSAMIStyle::GetSelectedStyle method


## -description



          Gets the current style from the SAMI media source.
        


## -parameters




### -param ppwszStyle [out]


            Receives a pointer to a null-terminated string that contains the name of the style. If no style is currently set, the method returns an empty string. The caller must free the memory for the string by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. 
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c4887c52-57af-4783-b853-11fe6ad3510e">IMFSAMIStyle</a>



<a href="https://msdn.microsoft.com/007c8181-089e-4e56-a31d-9d1942f90b07">SAMI Media Source</a>
 

 

